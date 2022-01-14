# Desafio 02 - Refactoring de classes e typescript

# 💻 Sobre o desafio

Nesse desafio, você deverá criar uma aplicação para treinar o que aprendeu até agora no ReactJS

Essa será uma aplicação já funcional onde o seu principal objetivo é realizar dois processos de migração: de Javascript para Typescript e de Class Components para Function Components.

A seguir veremos com mais detalhes o que e como precisa ser feito 🚀

## Template da aplicação

Para realizar esse desafio, criamos para você esse modelo que você deve utilizar como um template do GitHub.

O template está disponível na seguinte URL:
[template](https://github.com/rocketseat-education/ignite-template-reactjs-refactoring-classes-ts)

**Dica**: Caso não saiba utilizar repositórios do GitHub como template, temos um guia em **[nosso FAQ](https://www.notion.so/FAQ-Desafios-ddd8fcdf2339436a816a0d9e45767664).**

## Se preparando para o desafio

Para esse desafio, além dos conceitos vistos em aula utilizaremos o JSON server para criar uma Fake API com os dados das comidas.

### Fake API com JSON Server

Assim como utilizamos o MirageJS no módulo 2 para simular uma API com os dados das transações da aplicação dt.money, vamos utilizar o JSON Server para simular uma API que possui as informações das comidas.

Navegue até a pasta criada, abra no Visual Studio Code e execute os seguintes comandos no terminal:

```bash
yarn
yarn server
```

Em seguida, você vai ver a mensagem:

![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fc36df318-fb33-4a83-9d58-8f75b9be249c%2FUntitled.png?table=block&id=f0838129-b592-423b-bb95-fdc7dc982c88&spaceId=08f749ff-d06d-49a8-a488-9846e081b224&width=1080&userId=f7a3d1e0-5b3e-4fbc-8cd1-3b576bfe65ab&cache=v2)

Perceba que ele iniciou uma fake API com o recurso `/foods` em `localhost` na porta `3333` a partir das informações do arquivo [server.json](https://github.com/rocketseat-education/ignite-template-reactjs-refactoring-classes-ts/blob/master/server.json) localizado na raiz do seu projeto. Acessando essa rota no seu navegador, você consegue ver o retorno das informações já em JSON:

![](https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fbc8fd976-5a03-453d-8510-cf8a6925d4e8%2FUntitled.png?table=block&id=9ecb7f94-78b0-4ec8-aabe-628b1e120275&spaceId=08f749ff-d06d-49a8-a488-9846e081b224&width=2000&userId=f7a3d1e0-5b3e-4fbc-8cd1-3b576bfe65ab&cache=v2)

Dessa forma, basta consumir essas rotas da API normalmente com o Axios. Caso queira estudar mais sobre o **JSON Server**, dê uma olhada aqui:
[typicode/json-server](https://github.com/typicode/json-server)

## O que devo editar na aplicação?

Com o template já clonado, as depêndencias instaladas e a [fake API rodando](https://www.notion.so/Desafio-02-Refactoring-de-classes-e-typescript-4571541e7f8c4799bd191b6cfb53802c), você deve editar os seguintes arquivos:

- src/components/Food/index.jsx;
- src/components/Food/styles.js;
- src/components/Header/index.jsx;
- src/components/Header/styles.js;
- src/components/Input/index.jsx;
- src/components/Input/styles.js;
- src/components/Modal/index.jsx;
- src/components/ModalAddFood/index.jsx;
- src/components/ModalAddFood/styles.js;
- src/components/ModalEditFood/index.jsx;
- src/components/ModalEditFood/styles.js;
- src/pages/Dashboard/index.jsx;
- src/pages/Dashboard/styles.js;
- src/routes/index.jsx;
- src/services/api.js;
- src/styles/global.js;
- src/App.js;
- src/index.js.

Todos esses arquivos devem ser migrados de Javascript para Typescript. Além disso, os arquivos que possuírem componentes em classe devem ser migrados para componentes funcionais.

## Preparando ambiente Typescript

Como esse é um projeto CRA sem TypeScript, você primeiro precisar instalar as dependências/tipagens e configurar o TS. Nossa sugestão é criar um novo projeto CRA com Typescript e comparar a estrutura atual com a que você precisa ter. Realizando essa comparação, facilmente você consegue ver que:

- É preciso instalar o `typescript`
- É preciso criar um arquivo de configuração `tsconfig.json`. Inclusive, você pode utilizar a configuração gerada automaticamente no CRA template Typescript para criar o seu arquivo.
- É preciso criar um arquivo `react-app-env.d.ts` com o conteúdo:

```tsx
/// <reference types="react-scripts" />
```

- É preciso instalar as tipagens das bibliotecas.

Configurando esse setup, você deve ser capaz de trabalhar normalmente com o Typescript no seu projeto.

## Estou com dificuldade na conversão classes→função

Caso você tenha dificuldade nesse processo de migração, dê uma olhada no nosso guia sobre esse assunto:

[Componentes no React](https://www.notion.so/Componentes-no-React-6644d41da663405cb29dcaae1693bb9f)

## Como deve ficar a aplicação ao final?

Nesse desafio você já recebe a aplicação totalmente funcional, então todos os recursos mostrados no vídeo abaixo já estão implementados no template e devem permanecer funcionado após suas alterações.

[vídeo do app](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d7d94fcf-b6af-40eb-a215-731ac274e475/Peek_2021-03-10_10-43.mp4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220114%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220114T221251Z&X-Amz-Expires=86400&X-Amz-Signature=5dac76eaaa0fbd48fd82b65ef3f64cac26d2c00ec3e1d2b622cff4a8a7a8c4ab&X-Amz-SignedHeaders=host&x-id=GetObject)
