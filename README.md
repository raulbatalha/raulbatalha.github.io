# Iniciar o tema remoramente Minimal Mistakes

Este repositório serve como ponto de partida para quem deseja iniciar rapidamente com o tema [Minimal Mistakes para Jekyll](https://github.com/mmistakes/minimal-mistakes).

Inclui uma configuração básica para criar um site com:

- **Postagens de exemplo**: Demonstrações de como criar e exibir posts.
- **Navegação no topo**: Links principais para facilitar o acesso.
- **Barra lateral do autor**: Inclui informações sociais e sobre o autor.
- **Links no rodapé**: Personalizáveis para suas necessidades.
- **Página inicial paginada**: Organização eficiente das postagens.
- **Páginas de arquivo**: Posts agrupados por ano, categoria e tags.
- **Página "Sobre" de exemplo**: Para adicionar informações sobre você ou o site.
- **Página 404 de exemplo**: Para redirecionar usuários de forma elegante em páginas não encontradas.
- **Busca global no site**: Para facilitar a navegação e pesquisa de conteúdo.

Basta substituir o conteúdo de exemplo pelo seu e [configurar conforme necessário](https://mmistakes.github.io/minimal-mistakes/docs/configuration/).

---

## Solução de Problemas

Se tiver dúvidas sobre o uso do Jekyll, consulte os seguintes recursos:  

- Inicie uma discussão no [Fórum do Jekyll](https://talk.jekyllrb.com/) ou no [StackOverflow](https://stackoverflow.com/questions/tagged/jekyll).
- [Ruby 101](https://jekyllrb.com/docs/ruby-101/) para entender os fundamentos do Ruby, linguagem base do Jekyll.
- [Configuração de um site Jekyll com GitHub Pages](https://jekyllrb.com/docs/github-pages/).
- [Configuração dos Metadados do GitHub](https://github.com/jekyll/github-metadata/blob/master/docs/configuration.md#configuration).
---

## Organização do Código

Para manter o código organizado e de fácil manutenção, siga estas sugestões:

1. **Estrutura de Pastas**
   - `/_posts`: Armazene todas as postagens no formato `YYYY-MM-DD-titulo.md`.
   - `/assets`: Guarde imagens, arquivos CSS personalizados e scripts.
   - `/_config.yml`: Centralize as configurações principais do site.
   - `/pages`: Inclua páginas personalizadas, como "Sobre", "Contato", etc.

2. **Configuração Modular**
   - Use o arquivo `_config.yml` para gerenciar parâmetros globais, como título do site, descrição e links sociais.
   - Crie arquivos adicionais em `_data/` para organizar configurações específicas, como links de navegação e autores.

3. **Customização**
   - Use o diretório `_includes` para adicionar ou modificar partes específicas do tema.
   - Utilize o `_sass/` para ajustes no estilo.

4. **Teste Local**
   - Use o comando `bundle exec jekyll serve` para rodar o site localmente e testar alterações antes de publicar.

5. **Documentação**
   - Inclua um README atualizado no seu repositório com detalhes específicos do seu projeto.

Com essas melhorias, você terá um repositório organizado e um site bem configurado para atender às suas necessidades! 🚀