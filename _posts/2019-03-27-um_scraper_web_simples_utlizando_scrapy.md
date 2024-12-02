---
title: "Scraper Web Simples Utilizando Scrapy"
categories:
  - posts
tags:
  - web_scraping
---

Neste tutorial, vamos explorar o fluxo geral de um *web scraper* simples utilizando **Scrapy**, uma biblioteca popular em Python para raspagem de dados da web. O foco principal será sobre dois mecanismos essenciais do Scrapy para extrair informações a partir de dados HTML: **CSS Selector** e **XPath**.

# Fluxo Geral do Pipeline

Primeiro, explicarei rapidamente o fluxo básico de uma classe *Spider* que extrai citações de duas URLs, como mostrado no código abaixo. Para visualização, uma versão simples dos arquivos HTML baixados dessas duas URLs será semelhante ao seguinte:

```html
# Arquivo HTML retirado de https://docs.scrapy.org
<div class="quote">
    <span class="text">“O mundo como nós o criamos é um processo do nosso
    pensamento. Não pode ser mudado sem mudar nosso pensamento.”</span>
    <span>
        por <small class="author">Albert Einstein</small>
        <a href="/author/Albert-Einstein">(sobre)</a>
    </span>
    <div class="tags">
        Tags:
        <a class="tag" href="/tag/change/page/1/">change</a>
        <a class="tag" href="/tag/deep-thoughts/page/1/">deep-thoughts</a>
        <a class="tag" href="/tag/thinking/page/1/">thinking</a>
        <a class="tag" href="/tag/world/page/1/">world</a>
    </div>
</div>
```

Para extrair informações desse arquivo HTML, precisamos escrever uma classe Spider como o exemplo abaixo. A variável interna **`start_urls`** nessa classe define um conjunto de URLs a partir das quais os dados serão raspados. O Scrapy automaticamente enviará requisições HTTP para essas URLs, e quando a resposta estiver disponível, chamará a função **`parse`**.

O principal desafio agora será como extrair as informações desejadas dessa resposta, o que é feito pela função **`parse`** utilizando *CSS selectors*, que será abordado no próximo tópico.

```python
# Código retirado de https://docs.scrapy.org
import scrapy

class QuotesSpider(scrapy.Spider):
    name = "quotes"
    start_urls = [
        'http://quotes.toscrape.com/page/1/',
        'http://quotes.toscrape.com/page/2/',
    ]

    def parse(self, response):
        for quote in response.css('div.quote'):
            yield {
                'text': quote.css('span.text::text').get(),
                'author': quote.css('small.author::text').get(),
                'tags': quote.css('div.tags a.tag::text').getall(),
            }
```

# CSS Selector

Dentro da função **`parse`**, uma divisão **`quote`** é localizada com a seguinte consulta, que retorna todo o bloco HTML sob o elemento **`div`** com a classe **`quote`**:

```python
response.css('div.quote')
```

O texto da citação é então obtido pela regra:

```python
quote.css('span.text::text')
```

Primeiro, ela busca o elemento **`span`** com a classe **`text`**, e então acessa a propriedade **`text`** desse elemento.

O mesmo processo é aplicado aos campos **`author`** e **`tags`**.

Agora você tem uma visão geral de como os dados são baixados e como as informações são extraídas utilizando *CSS selectors*. Além disso, o Scrapy também oferece um mecanismo de consulta chamado **XPath**, que permite localizar praticamente qualquer elemento HTML em uma página da web.

# XPath Query

XPath é baseado em expressões de caminho para navegar entre elementos e atributos de um arquivo XML. Por exemplo, a consulta XPath para localizar o último elemento de livro do bloco HTML abaixo é mostrada a seguir.

```html
# Consulta XPath para o último elemento de livro
/bookstore/book[last()]
```

```html
# Dados retirados de https://www.w3schools.com
<bookstore>
<book category="cooking">
  <title lang="en">Everyday Italian</title>
  <author>Giada De Laurentiis</author>
  <year>2005</year>
  <price>40.00</price>
</book>
<book category="children">
  <title lang="en">Harry Potter</title>
  <author>J K. Rowling</author>
  <year>2005</year>
  <price>29.99</price>
</book>
</bookstore>
```

O XPath também é muito flexível para selecionar elementos filhos. Por exemplo, a seguinte consulta busca todos os elementos **`book`** cujo filho **`price`** seja maior que 35.0:

```html
/bookstore/book[price>35.0]
```

O exemplo a seguir mostra como carregar um arquivo HTML e aplicar uma consulta XPath usando Scrapy:

```python
path = './data/bookstore.html'
with open(path, 'r') as file:
    body = file.read()
    book = Selector(text=body).xpath('//bookstore/book[price>35]').get()
    print(book)
```

O resultado da consulta será:

```html
<book category="cooking">
  <title lang="en">Everyday Italian</title>
  <author>Giada De Laurentiis</author>
  <year>2005</year>
  <price>40.00</price>
</book>
```

# Combinação de CSS Selector e XPath

Em contraste com XPath, o *CSS selector* utiliza padrões para procurar elementos com estilos aplicados. Enquanto a consulta XPath requer um caminho até o elemento que queremos acessar, o CSS é mais flexível, pois permite definir elementos com base em suas classes ou atributos. Isso significa que consultas complexas podem ser simplificadas ao combinar *CSS selectors* e XPath.

Exemplo de HTML:

```html
<html>
 <head>
  <base href='http://example.com/' />
  <title>Website Exemplo</title>
 </head>
 <body>
  <div id='images'>
   <a href='image1.html'>Nome: Minha imagem 1 <br /><img src='image1_thumb.jpg' /></a>
   <a href='image2.html'>Nome: Minha imagem 2 <br /><img src='image2_thumb.jpg' /></a>
   <a href='image3.html'>Nome: Minha imagem 3 <br /><img src='image3_thumb.jpg' /></a>
   <a href='image4.html'>Nome: Minha imagem 4 <br /><img src='image4_thumb.jpg' /></a>
   <a href='image5.html'>Nome: Minha imagem 5 <br /><img src='image5_thumb.jpg' /></a>
  </div>
 </body>
</html>
```

Por exemplo, uma busca por todos os elementos **`src`** nas imagens do HTML acima pode ser feita com a seguinte consulta:

```python
response.css('img').xpath('@src').get()
```

O resultado será uma lista dos links relativos das imagens:

```html
['image1_thumb.jpg',
 'image2_thumb.jpg',
 'image3_thumb.jpg',
 'image4_thumb.jpg',
 'image5_thumb.jpg']
```

# Conclusão

Neste artigo, expliquei o fluxo geral de uma *Spider* simples do Scrapy e os dois mecanismos para extrair informações de arquivos HTML. A abordagem XPath estrutura uma consulta como um caminho entre os nós pais e filhos, enquanto o *CSS selector* localiza elementos com base em suas classes ou atributos. Ambos os mecanismos podem ser combinados para formar consultas mais complexas.

# Referências

[1] https://docs.scrapy.org