Aqui está o `README.md` formatado, pronto para copiar e colar:

```markdown
# Node.js Bootstrap Project

Este repositório contém um projeto inicial de Node.js já configurado com TypeScript, ESLint, Prettier, Jest, Husky, lint-staged e Commitlint. O projeto tem como objetivo facilitar a configuração inicial de novos projetos com todas essas ferramentas de qualidade de código.

## Pré-requisitos

- Node.js instalado
- npm ou yarn instalado

## Instalação

Para começar, instale todas as dependências do projeto:

```bash
npm install
```

## Scripts Disponíveis

- `format`: Formata os arquivos no diretório `src` usando o Prettier.
  ```bash
  npm run format
  ```

- `lint`: Executa o ESLint para verificar problemas no código.
  ```bash
  npm run lint
  ```

- `lint:fix`: Executa o Prettier e o ESLint para formatar e corrigir problemas no código.
  ```bash
  npm run lint:fix
  ```

- `test`: Executa todos os testes unitários e de integração.
  ```bash
  npm run test
  ```

- `test:unit`: Executa apenas os testes unitários.
  ```bash
  npm run test:unit
  ```

- `test:integration`: Executa apenas os testes de integração.
  ```bash
  npm run test:integration
  ```

- `test:staged`: Executa os testes apenas nos arquivos que estão preparados para commit.
  ```bash
  npm run test:staged
  ```

- `test:ci`: Executa todos os testes e gera um relatório de cobertura de código.
  ```bash
  npm run test:ci
  ```

- `test:coveralls`: Executa `test:ci` e envia o relatório de cobertura para o Coveralls.
  ```bash
  npm run test:coveralls
  ```

- `prepare`: Script executado automaticamente pelo Husky para preparar o ambiente de hooks.
  ```bash
  npm run prepare
  ```

## Husky e lint-staged

Este projeto usa Husky e lint-staged para garantir que todos os commits sigam as regras de formatação e qualidade de código.

### Hooks do Husky

- **pre-commit**: Executa o `lint-staged` para formatar e testar os arquivos preparados para o commit.
- **pre-push**: Executa todos os testes antes de permitir o push.
- **commit-msg**: Verifica se a mensagem do commit segue os padrões especificados no Commitlint.

### Configuração do lint-staged

```json
{
  "*.ts": [
    "npm run lint:fix",
    "npm run test:staged"
  ]
}
```

## Estrutura do Projeto

```bash
.
├── .husky/
├── coverage/
├── node_modules/
├── src/
├── tests/
├── .editorconfig
├── .gitignore
├── .lintstagedrc.json
├── .prettierrc
├── .prettierignore
├── commitlint.config.js
├── eslint.config.mjs
├── jest.config.ts
├── jest.integration.config.ts
├── jest.unit.config.ts
├── package-lock.json
├── package.json
├── tsconfig.build.json
└── tsconfig.json
```

## Contribuindo

Sinta-se à vontade para abrir issues e enviar pull requests para contribuir com este projeto.

## Licença

Este projeto está licenciado sob a licença ISC. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

```

---

Este arquivo `README.md` contém todas as informações necessárias para começar a usar o projeto, incluindo uma explicação dos scripts disponíveis, a configuração do Husky e `lint-staged`, e a estrutura do projeto.
