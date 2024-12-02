---
title: Automação de Testes Mobile com Appium e Selenium
excerpt: Uma solução modular para automação de testes em aplicativos móveis para Android e iOS, com captura de evidências e relatórios automatizados.
header:
  teaser: assets/images/automation_mobile_app/python_&_appium.jpeg
sidebar:
  - title: "Role"
    text: "Engenheiro de Qualidade de Software"
  - title: "Responsibilities"
    text: "Desenvolver e manter scripts de teste, configurar o ambiente de testes, e implementar captura de evidências automatizadas."
---

## Automação de Testes Mobile com Appium e Selenium

A automação de testes é uma peça-chave para garantir a qualidade em aplicações móveis. Este projeto utiliza as ferramentas Appium e Selenium para criar uma estrutura escalável, suportando dispositivos Android e iOS, com modularidade e captura automática de evidências.

### Por que este projeto é útil?

A automação manual de testes pode consumir muito tempo e recursos, especialmente em projetos que envolvem múltiplas plataformas. Este framework simplifica o processo, oferecendo:

- **Compatibilidade Multi-Plataforma**: Suporte para Android e iOS.
- **Relatórios Automatizados**: Relatórios HTML claros e organizados.
- **Evidências Visuais**: Captura automática de screenshots durante os testes.

---

### Estrutura Modular do Projeto

O projeto é organizado para ser intuitivo e fácil de manter. Aqui está uma visão geral:

```
/tests
    /pages                   # Representação das telas do aplicativo
    /tests                   # Arquivos de testes automatizados
    /utils                   # Funções auxiliares como captura de screenshots
    /evidencias              # Evidências geradas pelos testes
/config
    app_config.json          # Configuração para dispositivos e plataformas
```

Por exemplo, o arquivo `base_page.py` encapsula métodos genéricos reutilizáveis, enquanto `transactions_tests.py` implementa os testes específicos.

---

### Configuração Simples

1. **Atualize o `app_config.json`**:
   Configure os dispositivos e plataformas que serão usados nos testes, incluindo nome, versão e caminho do aplicativo.

   ```json
   {
     "platforms": [
       {
         "name": "Android",
         "version": "12.0",
         "deviceName": "Pixel_4_Emulator",
         "appPath": "app/budgetwatch.apk"
       }
     ]
   }
   ```

2. **Inicie o Appium Server**:
   Certifique-se de que o servidor Appium está rodando corretamente antes de executar os testes:

   ```bash
   appium --base-path /wd/hub 
   ```

3. **Execute os Testes**:
   Com tudo configurado, inicie os testes com o comando:

   ```bash
   pytest --html=report.html
   ```

---

### Principais Funcionalidades

- **Page Object Model (POM)**: Arquitetura modular para fácil manutenção.
- **Captura de Evidências**: Captura screenshots automaticamente para referência.
- **Relatórios HTML**: Relatórios detalhados e organizados com pytest-html.
- **Centralização de Dados**: Uso de arquivos JSON para entrada de dados dinâmicos.

---

### Contribuições Bem-Vindas!

Você pode contribuir com melhorias para este projeto. Siga os passos abaixo:

1. Faça um fork do repositório.
2. Crie um novo branch: `git checkout -b minha-feature`.
3. Commit suas alterações: `git commit -m "Minha contribuição"`.
4. Envie para o branch principal: `git push origin minha-feature`.
5. Crie uma Pull Request com suas alterações.

---

### Licença

Este projeto está licenciado sob a [MIT License](LICENSE). MIT © [Raul Batalha](https://github.com/raulbatalha).