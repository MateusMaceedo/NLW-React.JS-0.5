<h1 align="center">
<img src="https://xesque.rocketseat.dev/platform/1586184755042.svg" width="110" height="110">
 <br>
</h1>

[Configurações do ambiente](https://www.notion.so/Configura-es-do-ambiente-6dd0c69e71e141ef9492b00ba310a2fe)

# Introdução

Fala Dev! Seja muito bem vindo à **Next Level Week 05**, trilha **ReactJS** 🚀 

Para começar a preparar você para essa semana incrível de muito conteúdo e aprendizado, vamos começar configurando nosso ambiente de desenvolvimento, com algumas ferramentas fundamentais para chegarmos no fim desse evento com nosso app finalizado.

## Preparando o ambiente

Sem mais delongas, vamos ao conteúdo principal desse guia: configuração do seu ambiente para o NLW. Teremos três etapas principais na seção "**Instalação"**:

- Node + NPM;
- Yarn;
- Visual Studio Code e configurações.

Se você já participou de alguma das nossas outras NLWs, já deve ter tudo isso instalado, mas talvez desatualizado. Por isso, preparamos uma seção "**Atualização"** para você atualizar suas dependências caso precise, mas sugerimos dar uma olhada pelo menos no guia Visual Studio Code na seção "**Instalação"** pois o Diego deixou algumas configs especialmente para você 💜

Preparados? Então vamos lá!

![https://media.giphy.com/media/cPfjwUZtwArxyHVqjz/giphy.gif](https://media.giphy.com/media/cPfjwUZtwArxyHVqjz/giphy.gif)

---

# Guias

[Instalação das ferramentas](https://www.notion.so/Instala-o-das-ferramentas-405f3e8b014649cbb422dee6b5bd0535)

[Atualização (versões diferentes)](https://www.notion.so/Atualiza-o-vers-es-diferentes-09abff4d88d44c459a7c7a925ad15bfa)

[Tive problemas, e agora?](https://www.notion.so/Tive-problemas-e-agora-c67378e1319d4723a3211aad8eb987c6)

# Opcional - Configurações adicionais do VS Code

Se você já configurou todo o ambiente seguido os passos anteriores e quer deixar o Visual Studio Code com as mesmas configurações usadas pelo Diego nessa trilha, aqui vão algumas dicas:

## Extensões

Você pode instalar as seguintes extensões a partir do menu de extensões do próprio VS Code:

- **[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)**: Essa extensão faz a correção ortográfica no nosso código, funcionando melhor com camelcase (por padrão, corrige apenas o inglês). Essa extensão é bastante útil mas é totalmente opcional;
- **[Portuguese - Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-portuguese)**: É um dicionário de português para que a extensão **Code Spell Checker** consiga fazer também a correção ortográfica em Português;
- **[Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)**: Essa extensão reconhece cores CSS escritas em qualquer lugar do nosso código. Por padrão reconhece apenas cores em hexadecimal mas você pode configurar para reconhecer cores no formato de palavras como `"red"` ou `"yellow"`. É uma extensão bastante útil, já que reconhece as cores diretamente no código;
- [**CSS Modules**](https://marketplace.visualstudio.com/items?itemName=clinyong.vscode-css-modules): Essa é uma extensão que fornece o autocomplete para CSS Modules. Recomendamos o uso dela já que vai te ajudar com o autocomplete;
- [**Tabnine**](https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode): O Tabnine é uma extensão que usa de inteligência artificial para identificar o contexto do código e fornecer o autocomplete. Suporta diversas linguagens incluindo JavaScript e TypeScript. Existe uma versão paga mas também é possível usar a versão gratuita da extensão.
Seu uso é totalmente opcional;
- [**vscode-styled-components**](https://marketplace.visualstudio.com/items?itemName=jpoissonnier.vscode-styled-components): Essa extensão fornece o syntax highlighting e intelliSense para a biblioteca [styled-components](https://styled-components.com/). Se você for utilizar essa biblioteca, o uso da extensão é bastante recomendado.

## Configurações do VS Code

As seguintes configurações podem ser acessadas no VS Code apertando `Ctrl + Shift + P` (ou `cmd +` , digitando `Preferences: Open Settings (JSON)` e entrando na opção encontrada:

<img src="https://www.notion.so/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F79aca06f-8252-4865-a00f-d557469bb025%2FUntitled.png?table=block&id=0112b040-1fb6-450a-bc97-40a4c3d47c62&width=1730&userId=a79ee7a5-4c57-4287-a676-083310e9d184&cache=v2" width="864" height="463">

No arquivo JSON que abriu, adicione as seguintes configurações (certifique-se de adicionar dentro das chaves `{}`):

```json
"terminal.integrated.fontSize": 14,

"editor.tabSize": 2,
"editor.fontSize": 16,
"editor.lineHeight": 26,
"editor.semanticHighlighting.enabled": false,

"editor.rulers": [80, 120],

"editor.codeActionsOnSave": {
  "source.fixAll.eslint": true
},

"files.exclude": {
  "**/.git": true,
  "**/.svn": true,
  "**/.hg": true,
  "**/CVS": true,
  "**/.DS_Store": true,
  // "**/node_modules": true
},

"files.associations": {
  ".sequelizerc": "javascript",
  ".stylelintrc": "json",
  ".prettierrc": "json",
  "*.tsx": "typescriptreact"
},

"typescript.tsserver.log": "verbose",
"material-icon-theme.activeIconPack": "nest",

"material-icon-theme.folders.associations": {
  "infra": "app",
  "entities": "class",
  "domain": "class",
  "schemas": "class",
  "typeorm": "database",
  "repositories": "mappings",
  "http": "container",
  "migrations": "tools",
  "modules": "components",
  "implementations": "core",
  "dtos": "typescript",
  "fakes": "mock",
  "websockets": "pipe",
  "protos": "pipe",
  "grpc": "pipe",
  "providers": "include",
  "subscribers": "messages",
  "useCases": "controller",
  "kafka": "scripts",
  "mappers": "meta",
  "_shared": "shared",
  "eslint-config": "tools",
  "kube": "kubernetes"
},

"material-icon-theme.files.associations": {
  "ormconfig.json": "database",
  "tsconfig.json": "tune",
  "*.proto": "3d",
  "*.webpack.js": "webpack"
},
"window.menuBarVisibility": "toggle",
"tabnine.experimentalAutoImports": true,
"cSpell.enableFiletypes": [
  "!asciidoc",
  "!c",
  "!cpp",
  "!csharp",
  "!go",
  "!handlebars",
  "!haskell",
  "!jade",
  "!java",
  "!latex",
  "!php",
  "!pug",
  "!python",
  "!restructuredtext",
  "!rust",
  "!scala",
  "!scss"
],
"cSpell.language": "en,pt",
"editor.suggestSelection": "first",
"cSpell.userWords": [
  "chakra",
  "middlewares",
  "prefetch",
  "rocketseat"
],
"workbench.productIconTheme": "fluent-icons",
"terminal.integrated.showExitAlert": false,

"splitHTMLAttributes.closingBracketOnNewLine": true,
"window.zoomLevel": 1
```
