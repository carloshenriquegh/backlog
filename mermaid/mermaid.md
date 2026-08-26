#review 

```mermaid
---
config:
  theme: dark
---
  graph TD; 
  A(Start)-->B(Do some stuff); 
  B(Take some rest)-->C(do more);
  click B "http://www.github.com" "LINK_TARGET"

```

[Mermaid Theming](https://mermaid.js.org/config/theming.html)

# 1. Mermaid Theme List

base (único tema personalizável)

dark

default

forest

mc

neo

neo-dark

neutral

# Visão TODO
```mermaid
---
config:
  theme: dark
  ticketBaseUrl: 'https://github.com/carloshenriquecrx/obsidian-vault-carlos7z/blob/master/resources/#TICKET#'
---

kanban
legend[Legenda]
    legendId1[Tarefa de baixissíma prioridade]@{ priority: 'Very Low'}
    legendId2[Tarefa de baixa prioridade]@{ priority: 'Low'}
    legendId3[Tarefa de alta prioridade]@{ priority: 'High'}
    legendId4[Tarefa de altissíma prioridade, atríbuida]@{ priority: 'Very High', assigned: 'Henrique'}
    legendId4[Tarefa de altissíma prioridade, atribuída e com ticket]@{ ticket: resources, assigned: 'Diego', priority: 'Very High'}

[In progress]
	id6[Create renderer so that it works in all cases. We also add som extra text here for testing purposes. And some more just for the extra flare.]


[Ready for deploy]
	id8[Design grammar]@{ assigned: 'knsv' }
	
[Ready for test]
	id4[Create parsing tests]@{ ticket: MC-2038, assigned: 'K.Sveidqvist', priority: 'High' }
    id66[last item]@{ priority: 'Very Low', assigned: 'knsv' }
    
[Done]
    id5[define getData]
    id2[Title of diagram is more than 100 chars when user duplicates diagram with 100 char]@{ ticket: MC-2036, priority: 'Very High'}
    id3[Update DB function]@{ ticket: MC-2037, assigned: knsv, priority: 'High' }

[Can't reproduce]
    id3[Weird flickering in Firefox]

```

Os links infelizmente não funcionam como deveriam. No github não apresentam função. Por hora a frustração foi suficiente para criar camadas de distração. Vou tentar procurar alternativa com o gpt.

```mermaid
---
config:
ticketBaseUrl: 'https://mermaidchart.atlassian.net/browse/#TICKET#'
theme: dark
---
kanban
  Todo
    [Create Documentation]
    docs[Create Blog about the new diagram]
  [In progress]
    id6[Create renderer so that it works in all cases. We also add som extra text here for testing purposes. And some more just for the extra flare.]
  id9[Ready for deploy]
    id8[Design grammar]@{ assigned: 'knsv' }
  id10[Ready for test]
    id4[Create parsing tests]@{ ticket: 'MC-2038', assigned: 'K.Sveidqvist', priority: 'High' }
    id66[last item]@{ priority: 'Very Low', assigned: 'knsv' }
  id11[Done]
    id5[define getData]
    id2[Title of diagram is more than 100 chars when user duplicates diagram with 100 char]@{ ticket: MC-2036, priority: 'Very High'}
    id3[Update DB function]@{ ticket: 'MC-2037', assigned: knsv, priority: 'High' }

  id12[Can't reproduce]
    id3[Weird flickering in Firefox]

```

O gpt sugeriu usar uma lista de links abaixo do kanban. E tentar a opção com `graph TD`. Ambos códigos que o chatgpt gerou não estão de acordo. O segundo do tipo `graph td` renderizou mas os links não funcionam


```mermaid
graph TD;
    A[Refatorar API] -->|Ver detalhes| B((https://meusite.com/api))
    C[Criar componente UI] -->|Ver detalhes| D((https://meusite.com/ui))

```

```mermaid
---
config: 
  theme: dark
---
graph TD;
    Home -->|Menu| Sobre;
    Home -->|Menu| Blog;
    Home -->|Menu| Contato;
    Blog --> Post1;
    Blog --> Post2;

```

## Fluxo de usuário
```mermaid
---
config:
  theme: dark
---
graph TD;
    A[Usuário entra no site] --> B[Seleciona um produto];
    B --> C[Adiciona ao carrinho];
    C --> D[Faz login];
    D -->|Sucesso| E[Finaliza compra];
    D -->|Erro| F[Exibe mensagem de erro];
```

# Diagrama de banco de Dados

A melhor opção até aqui.

```mermaid
---
config:
  theme: dark
---
erDiagram
    CAR ||--o{ NAMED-DRIVER : allows
    CAR {
        string registrationNumber PK
        string make
        string model
        string[] parts
    }
    PERSON ||--o{ NAMED-DRIVER : is
    PERSON {
        string driversLicense PK "The license #"
        string(99) firstName "Only 99 characters are allowed"
        string lastName
        string phone UK
        int age
    }
    NAMED-DRIVER {
        string carRegistrationNumber PK, FK
        string driverLicence PK, FK
    }
    MANUFACTURER only one to zero or more CAR : makes

```

# Opções para planejar atividades

## Diagrama de Fluxo

```mermaid
---
config:
  theme: dark
---
graph TD;
  A[Início] --> B[Definir requisitos];
  B --> C{Wireframe aprovado?};
  C -- Sim --> D[Desenvolver back-end];
  C -- Não --> E[Ajustar wireframe];
  D --> F[Desenvolver front-end];
  F --> G[Testes e deploy];

```

## Diagrama de estado

```mermaid
---
config:
  theme: dark
---
stateDiagram
    direction LR
    [*] --> A
    A --> B
    B --> C
    state B {
      direction LR
      a --> b
    }
    B --> D
```

```mermaid
---
config:
  theme: dark
---
stateDiagram-v2
    state if_state <<choice>>
    [*] --> IsPositive
    IsPositive --> if_state
    if_state --> False: if n < 0
    if_state --> True : if n >= 0
```

```mermaid
---
config:
  theme: dark
---
stateDiagram-v2
    [*] --> First
    state First {
        [*] --> second
        second --> [*]
    }

    [*] --> NamedComposite
    NamedComposite: Another Composite
    state NamedComposite {
        [*] --> namedSimple
        namedSimple --> [*]
        namedSimple: Another simple
    }
```

```mermaid
---
config:
  theme: dark
---
stateDiagram-v2
    [*] --> First
    First --> Second
    First --> Third

    state First {
        [*] --> fir
        fir --> [*]
    }
    state Second {
        [*] --> sec
        sec --> [*]
    }
    state Third {
        [*] --> thi
        thi --> [*]
    }

```
```mermaid
---
config:
  theme: dark
---
stateDiagram-v2
    [*] --> First

    state First {
        [*] --> Second

        state Second {
            [*] --> second
            second --> Third

            state Third {
                [*] --> third
                third --> [*]
            }
        }
    }
```

```
# 1. Backlog
now is 5:45 the time will go to 5:50 a moment of push



```mermaid

%%{
  init: {
    'theme': 'dark',
    'themeVariables': {
      'primaryColor': '#0d0da2',
      'primaryTextColor': '#ffffff',
      'primaryBorderColor': '#4000ff',
      'lineColor': '#ffffff',
      'secondaryColor': '#0d0da2',
      'tertiaryColor': '#0d0da2'
    }
  }
}%%

kanban
Backlog
	[Backlog]
    [Create Documentation]
    docs[Create Blog about the new diagram]
  
```

```mermaid

%%{
  init: {
    'theme': 'dark',
    'themeVariables': {
      'primaryColor': '#0d0da2',
      'primaryTextColor': '#ffffff',
      'primaryBorderColor': '#4000ff',
      'lineColor': '#ffffff',
      'secondaryColor': '#0d0da2',
      'tertiaryColor': '#0d0da2'
    }
  }
}%%

kanban
Backlog
	Março
	[Backlog]
    [Create Documentation]
    docs[Create Blog about the new diagram]

  
```
## Como configurar a base de modo customizado
```text

%%{
  init: {
    'theme': 'base',
    
    
    'themeVariables': {
    
      'primaryColor': '#0d0da2',
      Cor da célula da tarefa 
  
      'primaryTextColor': '#ffffff',
      Cor do texto
      
      'primaryBorderColor': '#4000ff',
      Bordas das celulas 
      
      'lineColor': '#ffffff',
      Não se aplica porque não há linhas
      
      'secondaryColor': '#000000',
      Não se aplica

      'tertiaryColor': '#0d0da2'
      Cor do quadrado de fundo maior.
    }
  }
}%%

```
# 2. Objetivo

# 3. Foco
# 4. Pronto para Deploy

# 5. Pronto para Teste

# 6. Concluído
# 7. Visão 3x3

ToDo, in progress, ready for deploy, ready for test, done, Can't reproduce

1.
2.
3.
4.

Adicionar e testar links (que podem levar ao numero da requisição exemplo: #001, #002, #003, #004, #005, etc)

Usar as indicações de prioridade (low, medium, high)
# Gantt
Mês dividido em 4 semanas. Adaptar este gráfico

```mermaid
---
config:
  theme: dark
---
gantt
    dateFormat  YYYY-MM-DD
    title       Adding GANTT diagram functionality to mermaid
    excludes    weekends
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Critical tasks
    Completed task in the critical line :crit, done, 2014-01-06,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :until isadded
    Functionality added                 :milestone, isadded, 2014-01-25, 0d

    section Documentation
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Last section
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h


```
