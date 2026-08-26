# discord badges
https://support.discord.com/hc/en-us/articles/360035962891-Profile-Badges-101

Aguardar 3 dias
feito no dia 26

# How to use CODEBLOCKS

Codeblocks allow you to show your code using a monospace font and colors that make it a lot easier to read.

__One line code (no colors available)__:
Write the code inside backticks (`ALT`+`9`+`6` on desktop), **like this**:
> \`<?php $what = 'No colors!'; ?>\`
And this is **the result**:
```<?php $what = 'No colors!'; ?>```
__Multi line code (colors available)__:
Write 3 backticks (`ALT`+`9`+`6` on desktop) to start, followed by the code language (php in the example below), than add a new line (`SHIFT`+`ENTER` on desktop), insert your code, and at the end, close the codeblock with another 3 backticks in a row, **like this**:
> \`\`\`php
> $where = 'here';
> echo "Hey, multi-coloured code is {$where}!";
> ?>\`\`\`
And this is **the result**:
```php
$where = 'here';
echo "Hey, multi-coloured code is {$where}!";
```

__Extra: highlight changes__
You can use multiline codeblocks to highlighting code changes using `diff` as code opener, than `-` or `+` at for removed or added code like this:

```diff
// This is my code
$var = 'hello';
-$something= 'hey';
-echo $something;
+echo 'hey';
?>
```


And this is **the result**:
```diff
// This is my code
$var = 'hello';
-$something= 'hey';
-echo $something;
+echo 'hey';
?>
```

## Long code?

You can split it using more codeblocks in multiple messages in a row, or use an external code share platform like: [SourceB code sharer](https://sourceb.in/)

# Discord supported Markdown input

## Formatação de texto

|    Text format     | Command (delete backticks or c/p only the content inside them) |
| :----------------: | :------------------------------------------------------------: |
|      *Italic*      |                           `*italic*`                           |
|      **Bold**      |                           `**bold**`                           |
| ***Bold Italics*** |                      `***Bold Italics***`                      |
| ~~Strikethrough~~  |                      `~~Strikethrough~~`                       |

## Títulos, Subtítulos e Subtexto (em cinza)

| Title size      | Command           |
| --------------- | ----------------- |
| # Title 1       | `# Title`         |
| ## Subtitle     | `# Subtitle`      |
| ### Subtitle 2  | `### Subtitle 2`  |
| #### Subtitle 3 | `#### Subtitle 3` |
| -# Subtext      | `-# Subtext`      |

## Masked Links

| Link               | Mask                           | Output                       |
| ------------------ | ------------------------------ | ---------------------------- |
| https://google.com | `[Google](https://google.com)` | [Google](https://google.com) |

## Lists

| List type                                       | command    |
| ----------------------------------------------- | ---------- |
| bullet-point-filled                             | `* item`   |
| bullet-point                                    | `- item`   |
| ident bullet-point<br>(add 2 spaces before `-`) | `  - item` |

# Codeblocks 

Digite 3 backticks usando `SHIFT` + `botão de acento agudo` (pressione o acento três vezes) e na frente, sem espaços, determine o tipo da linguagem. Por exemplo:

```html
<html>
<body>
</body>
</html>
```

Das linguagens suportadas:

 - abap ('_.abap'), 
 - ada ('.adb', '.ads', '_.ada'), 
 - ahk ('.ahk', '.ahkl'), 
 - apacheconf ('.htaccess', 'apache.conf', 'apache2.conf'), 
 - applescript ('_.applescript'), as ('_.as'), as3 ('_.as'), 
 - asy ('_.asy'), 
 - bash ('.sh', '.ksh', '.bash', '.ebuild', '_.eclass'), 
 - bat ('.bat', '.cmd'), 
 - befunge ('_.befunge'), 
 - blitzmax ('_.bmx'), 
 - boo ('_.boo'), 
 - brainfuck ('.bf', '.b'), 
 - c ('.c', '.h'), 
 - cfm ('.cfm', '.cfml', '_.cfc'), 
 - cheetah ('.tmpl', '.spt'), 
 - cl ('.cl', '.lisp', '_.el'), 
 - clojure ('.clj', '.cljs'), 
 - cmake ('_.cmake', 'CMakeLists.txt'), 
 - coffeescript ('_.coffee'), 
 - console ('_.sh-session'), 
 - control ('control'), 
 - cucumber ('_.feature'), 
 - cpp ('.cpp', '.hpp', '.c++', '.h++', '.cc', '.hh', '.cxx', '.hxx', '_.pde'), 
 - csharp ('_.cs'), 
 - css ('_.css'), 
 - cython ('.pyx', '.pxd', '_.pxi'), 
 - d ('.d', '.di'), 
 - delphi ('_.pas'), 
 - diff ('.diff', '.patch'), 
 - dpatch ('.dpatch', '.darcspatch'), 
 - duel ('.duel', '.jbst'),
 - dylan ('.dylan', '.dyl'), 
 - erb ('_.erb'), 
 - erl ('_.erl-sh'), 
 - erlang ('.erl', '.hrl'), 
 - evoque ('_.evoque'),
 - factor ('_.factor'), 
 - felix ('.flx', '.flxh'), 
 - fortran ('.f', '.f90'), 
 - gas ('.s', '.S'), 
 - genshi ('_.kid'), 
 - gitignore ('.gitignore'), 
 - glsl ('.vert', '.frag', '_.geo'), 
 - gnuplot ('.plot', '.plt'),
 - go ('_.go'), 
 - groff ('.(1234567)', '.man'), 
 - haml ('_.haml'), haskell ('_.hs'), 
 - html ('.html', '.htm', '.xhtml', '.xslt'), 
 - hx ('_.hx'), 
 - hybris ('.hy', '.hyb'), 
 - ini ('.ini', '.cfg'),
 - io ('_.io'), 
 - ioke ('_.ik'), 
 - irc ('_.weechatlog'), 
 - jade ('_.jade'), 
 - java ('_.java'), 
 - js ('_.js'), 
 - jsp ('_.jsp'), 
 - lhs ('_.lhs'), 
 - llvm ('_.ll'), 
 - logtalk ('_.lgt'), 
 - lua ('.lua', '.wlua'), 
 - make ('.mak', 'Makefile', 'makefile', 'Makefile.', 'GNUmakefile'), 
 - mako ('_.mao'), 
 - maql ('_.maql'), 
 - mason ('.mhtml', '.mc', '_.mi', 'autohandler', 'dhandler'), 
 - markdown ('_.md'), 
 - modelica ('_.mo'), 
 - modula2 ('.def', '.mod'), 
 - moocode ('_.moo'), 
 - mupad ('_.mu'), 
 - mxml ('_.mxml'), 
 - myghty ('_.myt', 'autodelegate'), 
 - nasm ('.asm', '.ASM'), 
 - newspeak ('_.ns2'), 
 - objdump ('_.objdump'), 
 - objectivec ('_.m'), 
 - objectivej ('_.j'), 
 - ocaml ('.ml', '.mli', '.mll', '.mly'), 
 - ooc ('_.ooc'), 
 - perl ('.pl', '.pm'), 
 - php ('.php', '.php(345)'), 
 - postscript ('.ps', '.eps'), 
 - pot ('.pot', '.po'), 
 - pov ('.pov', '.inc'), 
 - prolog ('.prolog', '.pro', '_.pl'), 
 - properties ('_.properties'), 
 - protobuf ('_.proto'), 
 - py3tb ('_.py3tb'), 
 - pytb ('_.pytb'), 
 - python ('.py', '.pyw', '.sc', 'SConstruct', 'SConscript', '.tac'), 
 - r ('_.R'), 
 - rb ('.rb', '.rbw', 'Rakefile', '.rake', '.gemspec', '.rbx', '.duby'), 
 - rconsole ('_.Rout'), 
 - rebol ('.r', '.r3'), 
 - redcode ('_.cw'), 
 - rhtml ('_.rhtml'), 
 - rst ('.rst', '.rest'), 
 - sass ('_.sass'), 
 - scala ('_.scala'), 
 - scaml ('_.scaml'), 
 - scheme ('_.scm'), 
 - scss ('_.scss'), 
 - smalltalk ('_.st'), 
 - smarty ('_.tpl'), 
 - sourceslist ('sources.list'), 
 - splus ('.S', '.R'), 
 - sql ('_.sql'), 
 - sqlite3 ('_.sqlite3-console'), 
 - squidconf ('squid.conf'), 
 - ssp ('_.ssp'), 
 - tcl ('_.tcl'), 
 - tcsh ('.tcsh', '.csh'), 
 - tex ('.tex', '.aux', '_.toc'), 
 - text ('_.txt'), 
 - v ('.v', '.sv'), 
 - vala ('.vala', '.vapi'), 
 - vbnet ('.vb', '.bas'), 
 - velocity ('.vm', '.fhtml'), 
 - vim ('_.vim', '.vimrc'), 
 - xml ('.xml', '.xsl', '.rss', '.xslt', '.xsd', '.wsdl'), 
 - xquery ('.xqy', '.xquery'), 
 - xslt ('.xsl', '.xslt'), 
 - yaml ('.yaml', '.yml')

## Adicionar título do arquivo que contém o código

Antes de iniciar o codeblock acrescente
`### header3`

É importante incluir o aviso [[#Block Quotes e mensagens especiais|especial de código]] , para ficar bem organizado, seguindo todas suas estruturas e só depois incluir os códigos.

```text
Comece a copiar a partir da linha de baixo! até o final
> ## < > Código XYZ
> Insira seu texto aqui
> Explicativo sobre a função do código e sua localização
> O código em si deve ficar fora do quote
### index.html
```html
<html>
	<body>
		<h1>
			Teste de codeblock do tipo html com identação
		</h1>
	</body>
</html>
```



## Diff marcar adição e subtração de linha

Use o caracter + sem espaços para indicar uma linha de código que entra
Use o caracter - sem espaços para indicar uma linha de código excluída

```diff
+linha de código que entra
-linha de código excluída
```


## Block Quotes e mensagens especiais

Atenção

```text
↓ Copie a partir da linha de baixo
> ## :warning: Atenção para xyz
> Insira seu texto aqui
↑ ate a linha de cima
```

Bug

```text
>>> ## :beetle: Bug X
Insira seu texto aqui
```


Chave

```text

```


Código

```text

```


Download

```text

```


Git Tree

```text

```


Ideia

```text

```


Information

```text

```


Link

```text

```


Manutenção

```text

```


Material

```text

```


Pesquisar

```text

```


Trilha/Roadmap

```text

```


Versão
```text

```

Reiniciar

```text

```



| Tema              | Entrada (ignore os backticks)                                                                                                                                                                                                                                                                                                                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Atenção           | `>>> ## :warning: Atenção para xyz<br>Insira seu texto aqui`                                                                                                                                                                                                                                                                                                                                                   |
| Bug               | `>>> ## :beetle: Bug X<br>Insira seu texto aqui`                                                                                                                                                                                                                                                                                                                                                               |
| Chave             | `>>> ## :closed_lock_with_key: Chave XYZ<br>Insira seu texto aqui`                                                                                                                                                                                                                                                                                                                                             |
| Código            | `>>> ## :jigsaw: Código XYZ<br>Insira seu texto aqui<br>Explicativo sobre a função do código e sua localização<br>O código em si deve ficar fora do quote`                                                                                                                                                                                                                                                     |
| Download          | `>>> ## :inbox_tray: [Download XYZ](https:google.com)<br>Insira seu texto aqui. Pode conter a versão ou outros detalhes do link`                                                                                                                                                                                                                                                                               |
| Ideia/Sugestão    | `>>> ## :bulb: Sugestão de ideia para alteração de XYZ<br>Insira seu texto aqui descrevendo sua ideia. Abaixo é importante colar um código, blueprint ou excalidraw`                                                                                                                                                                                                                                           |
| Information       | `>>> ## :star: [Informação importe sobre livros, foruns ou fonte de material confiável como o site do laracasts](https://google.com)<br>Insira seu texto aqui`                                                                                                                                                                                                                                                 |
| Link              | `>>> ## :link: [Descrever o título do link](https://google.com)<br>esse link leva para X`                                                                                                                                                                                                                                                                                                                      |
| Manutenção        | `>>> ## :tools: Manutenção de código por motivo XYZ<br>Descreva aqui a motivação da mudança. Deve seguir de estruturas de pastas: use no terminal BASH da raiz do projeto "cmd //c tree //f" copie e cole para um codeblock do tipo text.<br>Adicione também codeblocks antecedido do título do arquivo.extensão.<br>Se necessário adicione um excalidraw para demonstrar modelagem ou arquitetura do projeto` |
| Material          | `>>> ## :books: O que são esses Materiais abaixo?<br>Insira seu texto aqui explicando o que são os masked links abaixo e do se tratam`                                                                                                                                                                                                                                                                         |
| Pesquisar         | `>>> ## :mag: Procurar por arquivo ou linha X para alteração<br>É necessário explicar o que alterar a linha vai fazer. Pode vir seguida de um codeblock do tipo text explicitando o caminho`                                                                                                                                                                                                                   |
| Trilha/Roadmap    | `>>> ### :map: Trilha para aprender XYZ nível básico/intermediário/avançado<br>Contém os links dos materiais em dificuldade crescente. Explicar qual  o objetivo da trilha, onde ela começa e onde ela termina`                                                                                                                                                                                                |
| Versão            | `>>> ## :package: Versão X.X<br>É necessária Versão lançada em dd de mm de aaaa ou XXX para YYYY funcionar`                                                                                                                                                                                                                                                                                                    |
| Repetir/Reiniciar | `>>> ## :repeat: Reiniciar XXXX<br>Explicar porque é importante  reiniciar`                                                                                                                                                                                                                                                                                                                                    |

GIT TREE Caminho da pasta e Subpasta.
# Emotes de reação a agradecimentos

Clique em responder e depois digite `+:nomedoemoji:`
se não selecionar responder o comando adiciona a reação a ultima mensagem do chat.

:blue_heart: para respostas carinhosas
:candy: para problemas simples
:handshake: para problemas que requerem passo-a-passo
