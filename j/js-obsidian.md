# Dentro do cabelho de definição de tag (entre `---`)

## Perguntar nome do arquivo ao criar nova nota
`<%* const filename = await tp.system.prompt("Digite um nome para a nota") await tp.file.rename(fileName) *%>`

## Data de agora
`<% tp.date.now() %>`

## Data de criação (created) (recomendado)
`<% tp.file.creation_date("DD-MM-YYYY HH:mm") %>`

## Modificado em (updated)
`<% tp.file.last_modified_date("DD-MM-YYYY HH:mm") %>`

# Fora do cabeçalho de definição de tag

## Data de criação do arquivo

```JS
tp.file.content
tp.file.create_new(template: TFile ⎮ string, filename?: string, open_new: boolean = false, folder?: TFolder | string)
tp.file.creation_date(format: string = "YYYY-MM-DD HH:mm")
tp.file.cursor(order?: number)
tp.file.cursor_append(content: string)
tp.file.exists(filepath: string)
tp.file.find_tfile(filename: string)
tp.file.folder(absolute: boolean = false)
tp.file.include(include_link: string ⎮ TFile)
tp.file.last_modified_date(format: string = "YYYY-MM-DD HH:mm")
tp.file.move(new_path: string, file_to_move?: TFile)
tp.file.path(relative: boolean = false)
tp.file.rename(new_title: string)
tp.file.selection()
tp.file.tags
tp.file.title
```


## Nome do arquivo

Determinar nome do arquivo com base no momento atual da criação do arquivo (Pode usar um # antes para determinar como título principal)
```javascript
<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
```

## Navegação entre notas

Navegação entre notas (o padrão sempre deve ser YYYY-MM-DD) em todos os plugins relacionados (Calendar, Daily notes, Git, Templater)

Configurar os plugins Calendar, Daily notes, Git e Templater, com formatos yyyy-MM-DD e configurar Dataview com yyyy-MM-DD hh:mm

Os nomes das variaveis `fileDateYesterday` e `fileDateTomorrow` podem ser alterados.

O código pode ser reaproveitado para outros fins de navegação entre cabeçalhos de uma nota (html, mkd).

```js
<< [[<% fileDateYesterday =  tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|voltar]] | [[<% fileDateTomorrow = tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|avançar]] >>
```


## Data da ultima atualização

Incluir data da última atualização em algum local do arquivo. Por algum motivo o código se mostra *depreciado* retornando NaN devido ao dinâmico uso do %. 
Como alternativa usar o código (2) do dataview
1. 
```js
Data de Atualização <%+ tp.file.last_modified_date("YYYY-MM-DD HH:mm") %>
```

2. 

`_Data da última atualização  =dateformat(this.file.mtime, "yyyy-MM-dd HH:mm")_`



[Templater "Created" and "Modified" dates suddenly started having problems](https://forum.obsidian.md/t/templater-created-and-modified-dates-suddenly-started-having-problems/51031) #snippets #templater/date

[Blacksmith Gu](https://blacksmithgu.github.io/obsidian-dataview/annotation/metadata-pages/) #dataview 

[Template Date and Time not Updating using tp.file.last_mofied_date and warning popping up next to tp.file.creation_date](https://forum.obsidian.md/t/template-date-and-time-not-updating-using-tp-file-last-mofied-date-and-warning-popping-up-next-to-tp-file-creation-date/69254) #snippets #templater/date/momentjs 

[templater-date-module](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/date-module.html) #templater/date

[Moment.js Documentation](https://momentjs.com/docs/#/-project-status/) #momentjs 

[3 Amazing Obsidian Plugins Dataview, Outliner and Templater](https://www.youtube.com/watch?v=2234DXKbNgM&t=1973s) #dataview #templater/guide #obsidian/plugins 