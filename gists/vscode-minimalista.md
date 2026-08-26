# 1. *VSCode* com interface minimalista

O objetivo da alteração visual minimalista é diminuir a quantidade de elementos em tela para alcançar o menor nível de distração possível.

O foco e a produtividade, enquanto que o usuário interage com a interface, são os pontos de interesse que justificam a mudança.

É importante ressaltar que todas as funções dos elementos visuais subtraídos são acessíveis via linha de comando (`CTRL`+`SHIFT`+`P`) ou terminal (`CTRL`+`J`).

Segue a comparação entre a interface padrão e o resultado pós personalização.
<div align="center">
    
###### ![vscode-padrão](https://gist.github.com/user-attachments/assets/d926ebd8-d627-4aad-b869-f2f5f951e531) Figura 1. Demonstração da interface padrão do VSCode (clique para ampliar e melhorar a resolução). Fonte [sstatic.net](https://i.sstatic.net/SHo2g.png).

</div>
<div align="center">
    
###### ![vscode-minimalista](https://gist.github.com/user-attachments/assets/1a1a65d7-75af-4633-908e-30bf501550a1) Figura 2. Demonstração da interface minimalista (clique para ampliar e melhorar a resolução). Fonte arquivo pessoal.

</div>

# 1.1. *APC Customize UI* e versão do *VSCode*
*(Atualizado em 12 de Fevereiro de 2025)*

A partir da versão 1.94 do VSCode de setembro de 2024, a extensão APC Customize UI++ em uso nesta configuração quebrou e até a data atual não há correção.

Para evitar o problema é necessário instalar a versão 1.93.

# 1.2. Como instalar a versão 1.93 do VSCode e desabilitar a atualização

## 1.2.1. [Clique aqui](https://update.code.visualstudio.com/1.93.1/win32-x64-user/stable) para download da [versão 1.93](https://code.visualstudio.com/updates/v1_93) para windows.

> [!warning]
> 
> **Pós instalação**
> 
> Ao abrir a **primeira vez** o *VSCode* siga as instruções abaixo.

## 1.2.2. Pressione `Ctrl`+`Shift`+`P` digite `UI` clique em "*Preferences: Open Settings (UI)*" acesse "Aplicação (ou *Application*) > *Update*".
<div align="center">
    
###### ![ui](https://gist.github.com/user-attachments/assets/989f5ce3-5b8e-4854-9a81-32142b7831bf) <br>Figura 1. Como acessar preferências da aplicação. Fonte arquivo pessoal.

</div>
<div align="center">
        
###### ![ui-update](https://gist.github.com/user-attachments/assets/a242eca8-5dbc-4b67-8f31-d2b7c0e42165) <br> Figura 1.1. Como acessar preferências da aplicação. Fonte arquivo pessoal.

</div>

## 1.2.3. **DESMARQUE A OPÇÃO**: ▢ Habilitar update em segundo plano.

## 1.2.4. **MODO**: Escolha a opção **NENHUM**.

<div align="center">
    
###### ![update-mode](https://gist.github.com/user-attachments/assets/015992f7-4c52-4ee5-b4d4-18089660e342) <br> Figura 2. Demonstração de como configurar as preferências da aplicação (atenção para desmarcar a opção). Fonte arquivo pessoal.

</div>
    
## 1.2.5. Para conferir a versão do *VSCode* é bem simples. Com o programa aberto pressione `CTRL`+`SHIFT`+`P` e digite `help about` pressione `ENTER`. Versão (*user setup*) deve constar 1.93.1.

<div align="center">    

######  ![vscode-version](https://gist.github.com/user-attachments/assets/6a174d9d-70df-4c4a-b061-f0ccc9ab95ab) <br> Figura 3. Conferir versão. Fonte arquivo pessoal. 

</div>

## 1.2.6. O próximo passo é abrir o arquivo de configuração da interface. Para acessar o arquivo de configuração do VSCode pressione `CTRL`+`SHIFT`+`P` e digite `settings.json` e clique na primeira opção "*Open User Settings (JSON)*"

<div align="center">
    
###### ![settings.json](https://gist.github.com/user-attachments/assets/b92f3cb9-aec4-4690-9075-93120433389c) <br> Figura 4. Abrindo arquivo de configuração. Fonte arquivo pessoal.

</div>

## 1.2.7. Copie e cole o código abaixo no arquivo, sobreescrevendo o código existente.

```json

{
  "workbench.startupEditor": "newUntitledFile",
  "editor.fontSize": 20,
  "editor.lineHeight": 1.8,
  "javascript.suggest.autoImports": true,
  "javascript.updateImportsOnFileMove.enabled": "always",
  "editor.rulers": [
    80,
    120
  ],
  "extensions.ignoreRecommendations": true,
  "typescript.tsserver.log": "off",
  "editor.stickyScroll.enabled": false,
  "workbench.tree.enableStickyScroll": false,
  "files.associations": {
    ".env.*": "dotenv",
    ".prettierrc": "json",
    "*.css": "css",
    ".dev.vars": "dotenv"
  },
  "symbols.files.associations": {
    "*.module.ts": "nest",
    "*.guard.ts": "typescript",
    "*.spec.ts": "ts-test",
    "*.e2e-spec.ts": "ts-test",
    "*.mock.ts": "ts-test",
    "vitest.config.e2e.ts": "vite",
    ".env.development.local": "gear",
    ".env.test.local": "gear",
    ".env.local": "gear",
    ".env.example": "gear"
  },
  "tailwindCSS.experimental.classRegex": [
    [
      "tv\\(([^)]*)\\)",
      "[\"'`]([^\"'`]*).*?[\"'`]"
    ],
    "class:\\s*?[\"'`]([^\"'`]*).*?,"
  ],
  "editor.parameterHints.enabled": false,
  "editor.renderLineHighlight": "gutter",
  "cSpell.language": "en,pt",
  "typescript.updateImportsOnFileMove.enabled": "always",
  "editor.suggestSelection": "first",
  "explorer.confirmDelete": false,
  "gitlens.codeLens.recentChange.enabled": false,
  "terminal.integrated.showExitAlert": false,
  "[prisma]": {
    "editor.formatOnSave": true,
    "editor.formatOnPaste": true,
    "files.autoSave": "afterDelay",
    "files.autoSaveDelay": 1000
  },
  "typescript.suggest.autoImports": true,
  "typescript.preferences.preferTypeOnlyAutoImports": true,
  "terminal.integrated.env.osx": {
    "FIG_NEW_SESSION": "1"
  },
  "workbench.editor.labelFormat": "short",
  "workbench.sideBar.location": "right",
  "editor.fontLigatures": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "mdx": "javascriptreact"
  },
  "emmet.syntaxProfiles": {
    "javascript": "jsx",
    "mdx": "jsx"
  },
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
  "editor.acceptSuggestionOnCommitCharacter": false,
  "explorer.compactFolders": false,
  "git.enableSmartCommit": true,
  "editor.accessibilitySupport": "off",
  "explorer.confirmDragAndDrop": false,
  "terminal.integrated.fontSize": 20,
  "terminal.integrated.fontFamily": "JetBrainsMono Nerd Font",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit"
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "graphql"
  ],
  "editor.semanticHighlighting.enabled": false,
  "breadcrumbs.enabled": false,
  "workbench.productIconTheme": "fluent-icons",
  "editor.fontFamily": "JetBrains Mono",
  "gitlens.codeLens.authors.enabled": false,
  "editor.tabSize": 2,
  "security.workspace.trust.untrustedFiles": "newWindow",
  "files.exclude": {
    "**\/CVS": true,
    "**\/.DS_Store": true,
    "**\/.hg": true,
    "**\/.svn": true,
    "**\/.git": true,
    ".vscode": true,
  },
  "workbench.iconTheme": "symbols",
  "update.mode": "none",
  "terminal.integrated.gpuAcceleration": "on",
  "terminal.integrated.defaultProfile.osx": "fish",
  "[jsonc]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[json]": {
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "window.commandCenter": false,
  "git.openRepositoryInParentFolders": "always",
  "symbols.hidesExplorerArrows": false,
  "[javascript]": {
    "editor.defaultFormatter": "vscode.typescript-language-features"
  },
  "console-ninja.featureSet": "Community",
  "workbench.editor.empty.hint": "hidden",
  "update.showReleaseNotes": false,
  "security.promptForLocalFileProtocolHandling": false,
  "workbench.activityBar.location": "hidden",
  "apc.activityBar": {
    "position": "bottom",
    "hideSettings": true,
    "size": 48,
    "itemMargin": 8,
    "itemSize": 32
  },
  "editor.hideCursorInOverviewRuler": true,
  "editor.minimap.enabled": false,
  "window.titleBarStyle": "native",
  "apc.electron": {
    "titleBarStyle": "hidden",
    "frame": false,
    "opacity": 1,
    "vibrancy": "dark"
  },
  "apc.header": {
    "height": 40
  },
  "apc.listRow": {
    "height": 25
  },
  "apc.font.family": "Inter",
  "apc.stylesheet": {
    ".title-label > h2": "display: none",
    ".editor-actions": "display: none",
    ".nosidebar div.inline-tabs-placeholder": "width: 75px",
    ".pane-header": "padding: 0 8px",
    ".pane-body": "padding: 8px",
    ".split-view-view:first-child .pane-header": "display: none !important;",
    ".monaco-list-row": "border-radius: 4px;",
    ".monaco-workbench .monaco-list:not(.element-focused):focus:before": "display: none;"
  },
  "editor.scrollbar.vertical": "hidden",
  "explorer.sortOrder": "foldersNestsFiles",
  "explorer.fileNesting.patterns": {
    "package.json": ".eslint*, prettier*, tsconfig*, vite*, pnpm-*, bun.lockb, nest*, package-lock*",
    "tailwind.config.*": "tailwind.config*, postcss.config*",
    ".env.local": ".env*",
    ".env": ".env*"
  },
  "explorer.fileNesting.enabled": true,
  "cSpell.userWords": [
    "automations",
    "bootcamp",
    "chakra",
    "checkin",
    "checkins",
    "cloudflare",
    "clsx",
    "Codegen",
    "datadog",
    "Datetime",
    "dayjs",
    "Dotenv",
    "Elysia",
    "esbuild",
    "fastify",
    "Fastify",
    "feedbackwidget",
    "ffprobe",
    "gamificada",
    "Hasher",
    "hono",
    "Hono",
    "ilike",
    "IUGU",
    "jamjuree",
    "jupiter",
    "ksuid",
    "liveblocks",
    "LIVEBLOCKS",
    "Marguerita",
    "middlewares",
    "mixpanel",
    "monaco",
    "nestjs",
    "nivo",
    "omni",
    "Omni",
    "Onboarded",
    "pallas",
    "postgres",
    "postgresql",
    "prefetch",
    "reactflow",
    "retriable",
    "roboto",
    "rocketseat",
    "rotion",
    "rsxp",
    "Sandpack",
    "shiki",
    "skylab",
    "sqlite",
    "supergraph",
    "svgr",
    "sympla",
    "tailwindcss",
    "textblock",
    "tiptap",
    "trpc",
    "TRPC",
    "tsup",
    "unfollow",
    "Unfollow",
    "unform",
    "Unform",
    "unmark",
    "upsert",
    "Usuario",
    "webm",
    "WEBPUSH"
  ],
  "workbench.statusBar.visible": false,
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": "keyword.other.dotenv",
        "settings": {
          "foreground": "#FF000000"
        }
      }
    ]
  },
  "workbench.layoutControl.enabled": false,
  "window.autoDetectColorScheme": true,
  "workbench.preferredDarkColorTheme": "poimandres",
  "workbench.preferredLightColorTheme": "Min Dark",
  "gitlens.advanced.messages": {
    "suppressIntegrationRequestTimedOutWarning": true
  },
  "liveServer.settings.donotShowInfoMsg": true,
  "update.enableWindowsBackgroundUpdates": false,
  "terminal.integrated.env.windows": {},
  "workbench.editor.tabSizing": "shrink",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "window.customTitleBarVisibility": "never",
  "window.newWindowDimensions": "maximized",
  "window.restoreFullscreen": true,
  "window.menuBarVisibility": "hidden",
      "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}

```

### 1.2.8. Não se preocupe com sinalizações ou alertas no código, a resolução deste problema se faz na próxima seção.

### 1.2.9. Salve as alterações com `CTRL`+ `S`. 

### 1.2.10. Reinicie o *VSCode*.

# 2. Extensões

Para acessar as extensões do *VSCode* pressione `CTRL`+`SHIFT`+`P` e digite `install extensions` e clique na opção "*Extensions: Install Extensions*" e na janela que se abre digite as extensões que deseja instalar.

- *Apc Customize UI++*

- *Auto close Tag*

- *Auto Rename Tag*

- *C/C++*

- *C/C++ Extension Pack*

- *C/C++ Themes*

- *CMake*

- *CMake Tools*

- *Code Spell Checker*

- *Composer*

- *Console Ninja*

- *Fish*

- *GitLens - Git supercharged*

- *ESLint*

- *Fluent Icons*

- *Min Theme*

- *PHP Inteliphense*

- *PHP Server*

- *Poimandres*

- *Prettier - Code Formatter*

- *Prettier ESLint*

- *Prettier SQL VSCode*

- *Prisma*

- *Tailwind CSS IntelliSense*

# Extra

## 2.1. Extensões de preferência pessoal

Seguem configurações de preferência pessoal que não tem relação com as alterações de interface. Se possuir interesse em configurar o ambiente do *VSCode* (inclui variáveis de ambiente *windows*) para alguma linguagem das subseções desta seção pode seguir o passo a passo. 

## 2.2. Extensões Java para VSCode

Instalar o [*Extension Pack for Java*](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) que contém:

- *[Language Support for Java™ by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)*

- *[Debugger for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)*

- *[Test Runner for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-test)*

- *[Maven for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-maven)*

- *[Project Manager for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-dependency)*

- *[Visual Studio IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)*

### 2.2.1. Pacotes de codificação *jdk* (*Java Development Kit*)

Instalar [o pacote de codificação *Eclipse Adoptium*](https://aka.ms/vscode-java-installer-win). 

O *JDK* inclui ferramentas para compilar código-fonte em *bytecode*, empacotar aplicativos, iniciar máquinas virtuais *Java* (*Java Virtual Machine*), gerenciar o ambiente de execução de aplicativos *Java*, desenvolver e testar programas.

### 2.2.2. Configuração da variável de ambiente para que os comandos sejam reconhecidos no terminal do *VSCode*

1. Abra o terminal cmd no *Windows* e entre com os seguintes comandos na ordem:

`pushd C:\`

`for %i in (java.exe) do @echo. %~$PATH:i`

2. Você deve receber o diretório padrão como retorno:

`C:\Program Files\Eclipse Adoptium\jdk-17.0.14.7-hotspot\bin\java.exe`

3. Copie o endereço acima.

4. Pressione o botão Windows e digite "Variáveis de ambiente".

5. Na janela "Propriedades do sistema" que se abre clique em "Variáveis de ambiente." 

6. No topo da janela que se abre "Variáveis de usuário" clique duas vezes em "*Path*".

7. Clique em "Novo" cole o endereço que copiamos até o diretório "*bin*". Deve ficar assim:

`C:\Program Files\Eclipse Adoptium\jdk-17.0.14.7-hotspot\bin`

8. Clique em "*OK*" em todas as janelas abertas até aqui para confirmar a mudança. Feche o *VSCode* se estiver aberto.

9. Abra um novo terminal no *VSCode* (`CRTL`+`J`).

10. Execute o comando `java -version`. O comando deve retornar a versão.

# 3. Referências

Fernandes, Diego (janeiro de 2024). [Meu VSCode minimalista extensões, temas e config](https://www.youtube.com/watch?v=TW3KoPkuWEA). [Canal da Rocketseat no *youtube*](https://www.youtube.com/@rocketseat). Consultado em 12 de fevereiro de 2025.

Fernandes, Diego (outubro de 2024). [*Vs Code Settings (Updated)*](https://gist.github.com/diego3g/b1b189063d21b96d6144ca896755be64). [*Github gists* Diego Fernandes](https://gist.github.com/diego3g). Consultado em 12 de fevereiro de 2025.

*Visual Studio Code* (agosto de 2024). [*August 2024 version 1.93*](https://code.visualstudio.com/updates/v1_93). [*Visual Studio Code website*](https://code.visualstudio.com/). Consultado em 12 de fevereiro de 2025.

*Visual Studio Code* (março de 2025). [*Java in Visual Studio Code*](https://code.visualstudio.com/docs/languages/java). [*Visual Studio Code website*](https://code.visualstudio.com/). Consultado em 19 de março de 2025.

# Agradecimentos

Se gostou do material e ele foi útil de alguma forma, por gentileza clique na estrela :star: no canto superior direito da tela para favoritar o gist. Vou revisar, atualizar e melhorar a apresentação dos dados todo mês se possível. Os comentários construtivos e sugestões são sempre bem vindos. 

###### *"A gratidão é um antídoto contra a frustração e o desamparo." - Pedro Calabrez*


<hr>
# Melhorias

# Adicionar capitalização para inglês e corrigir todas as seções de acordo com a última versão do texto

# 1. APC Customize UI extension and VSCode version issue solution
*(Updated on February 12th 2025)*

Starting with version 1.94 the APC Customize UI++ extension in this config broke and there is no fix until this day.

To avoid the problem you need to install version 1.93.

## How to install version 1.93 and disable update

1. [Download](https://update.code.visualstudio.com/1.93.1/win32-x64-user/stable) (win) [version 1.93](https://code.visualstudio.com/updates/v1_93)

2. **IMPORTANT**: When opening VSCode for the **first time**, configure the following:

    File > Preferences > Settings > Application > Update 

    or with the shortcut `Ctrl`+`Shift`+`P` type `UI` access "Application > Update"

    **UNCHECK THE OPTION**: [ ] Enable background update

    **MODE**: Choose the option **NONE**.

3. To check the VSCode version, access the default address of the code.exe executable in

    `%USERPROFILE%\AppData\Roaming\VSCode.exe`

    or in the directory you chose during installation (you can also right click on the taskbar icon > properties > destination)

    Right-click on the file "code.exe > Properties > Details"

    The file/product version should be 1.93.1.0.
    
 4. To access the VSCode configuration file, press `CTRL`+`SHIFT`+`P` and type `settings.json` and click on the first option "Open user settings (json)"

    Copy and paste the code from `02-settings.json` present in this git.

# Sugestões de mudanças

## Abril 2025

20250404-0 imagem como apresentação do pinned (?) [Pixilart](https://www.pixilart.com/)

20250404-1 Substituir o link de imagem markdown por `<div><img src="" style="">...</img></div>`. Incluir bordas nas imagens.

20250404-2 Incuir seção **conteúdo**. A seção deve ter a opção de expandir/retrair.

20250404-3 Revisar todos os títulos e subtítulos para diminuir o número de índices. Revisar todo o texto. Alterar a seção 1.1. para "Extensão para configuração de interface APC Customize UI".

20250404-4 Substituir todos os passos de sequência por um gráfico *codeblock mermaid*. É importante que o conteúdo, principalmente os códigos, se houver, possam ser copiados do gráfico para área de transferência.

20250404-5 Imagem de apresentação. Pode conter *github badges*.

20250404-6 Opção para alternar o idioma para inglês (o *gist* não deve ser *pinned*, verificar viabilidade de exposição/acessibilidade via linking de ícone de bandeira clicável).

20250407-7 Verificar forma de renderizar as imagens no arquivo de origem (obsidian vault) e no arquivo de destino (github repo) afim de exibir o conteúdo nas duas páginas como o mesmo caminho relativo da imagem. Verificar se é possível carregar do repo privado. De acordo com [Embed image from GitHub private repo](https://stackoverflow.com/questions/63915756/embed-image-from-github-private-repo) seria por meio de token com `raw.githubusercontent` no início do endereço e final adicionar o número do token `token=xxxxxxxx`. Exibir o token não é uma opção. Também não faço ideia de como suprimir. Me agrada o fato de procurar outra solução.