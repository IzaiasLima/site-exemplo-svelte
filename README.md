# Site Exemplo Svelte

Exemplo de site, usando o framework de desenvolvimento de frontend **Svelte**. Este site foi desenvolvido com o propósito, apenas, de testar as funcionalidades e facilidades oferecidas por essa ferramenta de desenvolvimento.

Na parte de estilização, usamos o framework [Pico CSS](https://picocss.com/).  

Para saber mais sobre o framework utilizado, consulte https://svelte.dev/.

## Criando um projeto

Se você preferir iniciar um novo projeto, em vez de clonar este repositório:

```bash
# create a new project in the  frontend directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Para rodar em desenvolvimento

Criado o projeto e atualizadas as dependências com `npm install` (ou `pnpm install` ou `yarn`), inicie o servidor local:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

Para criar uma versão em produção:

```bash
npm run build
```

Se que quiser um preview do build de produção: `npm run preview`.

Para fazer o deploy em produção, veja a documentação do framework: https://kit.svelte.dev/docs/adapters.
