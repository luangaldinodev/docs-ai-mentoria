# Babel Idiomas

## Visão Geral

**Babel Idiomas** é um sistema projetado para ser uma plataforma de ensino de idiomas, com foco principal no aprendizado de inglês. Este projeto foi desenvolvido como parte de um trabalho escolar voltado para vendas, integrando funcionalidades como vídeos exclusivos e quizzes interativos. Também pode ser considerado um protótipo para um Trabalho de Conclusão de Curso (TCC).

## Funcionalidades Principais

- **Aulas em Vídeo**: Acesso a vídeos exclusivos com parceiros, proporcionando uma experiência de aprendizado personalizada.
- **Quiz Interativo**: Ferramenta para avaliação e fixação do conteúdo aprendido.
- **Interface Amigável**: Design simples e intuitivo para facilitar a navegação dos usuários.

## Tecnologias Utilizadas

### Front-end:
- **HTML**: Estruturação das páginas.
- **CSS**: Estilização e layout do sistema.

### Back-end:
- **PHP**: Processamento de dados e lógica de aplicação.
- **MySQL**: Banco de dados para armazenamento de informações.
- **JavaScript**: Utilizado para interatividade básica (e.g., exibição de alertas).

## Estrutura do Projeto

A seguir, a estrutura básica de diretórios do projeto:

```
├── /assets
│   ├── /css
│   ├── /images
│   └── /js
├── /includes
├── /pages
├── /sql
└── index.php
```

### Descrição dos Diretórios
- **/assets**: Contém os arquivos estáticos, como CSS, imagens e JavaScript.
- **/includes**: Contém arquivos PHP reutilizáveis, como cabeçalhos e rodapés.
- **/pages**: Contém as páginas dinâmicas do sistema.
- **/sql**: Scripts SQL para configuração do banco de dados.
- **index.php**: Página inicial do sistema.

## Requisitos do Sistema

- **Servidor Web**: Apache ou similar.
- **PHP**: Versão 7.4 ou superior.
- **Banco de Dados**: MySQL 5.7 ou superior.

## Configuração e Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/luangaldinodev/babel-idiomas.git
   ```

2. Configure o banco de dados:
   - Importe o arquivo SQL localizado em `/sql` para o seu servidor MySQL.

3. Atualize o arquivo de configuração do banco de dados:
   - No arquivo `config.php` (localizado em `/includes`), insira as credenciais do seu banco de dados.

4. Execute o projeto:
   - Coloque os arquivos do projeto no diretório raiz do seu servidor web.
   - Acesse `http://localhost/babel-idiomas` no navegador.

## Próximos Passos

- Melhorar a interatividade com JavaScript moderno.
- Implementar autenticação de usuários.
- Criar uma API para integração com serviços externos.

---

## Contribuição

Sinta-se à vontade para contribuir com este projeto enviando pull requests ou relatando problemas na aba Issues do repositório GitHub.

---

## Licença

Este projeto é distribuído sob a licença MIT. Para mais detalhes, consulte o arquivo LICENSE.
