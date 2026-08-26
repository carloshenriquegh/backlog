#review 

//www.mermaidchart.com/app/
# 1. A class sequence diagram with inheritance

```mermaid
---
config:
  theme: dark
---
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }

```
# 1. A class diagram using cardinalities

```mermaid
---
config:
  theme: dark
---
classDiagram
    %% Example showing the use of cardinalities

    %% Defining the classes
    class Company {
        +String name
        +String address
        +hireEmployee(Employee)
    }
    class Employee {
        +String firstName
        +String lastName
        +int employeeID
        +workFor(Company)
    }
    class Project {
        +String projectName
        +Date projectDeadline
        +addMember(Employee)
    }

    %% Defining the relationships with cardinalities
    Company "1" --> "1..*" Employee : employs
    Employee "1" --> "0..1" Company : works for
    Employee "1..*" --> "1" Project : is involved in
    Project "1" --> "0..*" Employee : has member

    %% Adding a note to explain the diagram
    note for Company "A Company employs one or more Employees."
    note for Employee "An Employee may work for a Company and is involved in one Project."
    note for Project "A Project has multiple Employees as members."

    %% Applying CSS classes using shorthand notation
    class Company:::companyStyle
    class Employee:::employeeStyle
    class Project:::projectStyle

    %% Apply CSS classes using cssClass statement
    %% cssClass "Company, Employee, Project" generalClass

     style Company fill:#f9f,stroke:#333,stroke-width:4px
     style Employee fill:#f9f,stroke:#333,stroke-width:4px
     style Project fill:#263,stroke:#66f,stroke-width:2px,color:#fff,stroke-dasharray: 5 5


```

# 2. Class schema for an issue tracking system with inheritance and interfaces

```mermaid
---
config:
  theme: dark
---
classDiagram
    class Issue {
        <<Abstract>>
        +int id
        +String title
        +String description
        +Status status
        +User assignedTo
        +start()
        +complete()
    }

    class Bug {
        +Severity severity
        +String report()
    }

    class Epic {
        +String featureDetails
        +requestApproval()
    }

    class Story {
        +int EpicID
    }

    class Task {
        +Date deadline
    }

    class User {
        <<Abstract>>
        +int userId
        +String username
        +String email
        +login()
        +logout()
    }
    
    class Admin {
        +manageUsers()
        +viewAllTasks()
    }

    class RegularUser {
        +viewAssignedTasks()
        +updateTaskStatus()
    }

    class TaskManager {
        <<interface>>
        +assignTask()
        +removeTask()
        +updateTask()
    }
    TaskManager <|.. TaskApp

    class TaskApp {
        +assignTask()
        +removeTask()
        +updateTask()
        +getAllTasks()
    }

    class Status {
        <<enumeration>>
        New
        Open
        In Progress
        Postponed
        Closed
    }

    class Severity {
        <<enumeration>>
        Critical
        High
        Medium
        Low
    }

    Issue "1" -->  User : assignedTo
    Issue "1" --> Status : has
    Bug "1" --> Severity : has
    Issue <|-- Bug : Inheritance
    Issue <|-- Epic : Inheritance
    Issue <|-- Task : Inheritance
    Issue <|-- Story : Inheritance
    Epic "0" --> "many" Story
    User <|-- Admin
    User <|-- RegularUser
    
    style Issue fill:#bfb,stroke:#6f6,stroke-width:2px,color:#000,stroke-dasharray: 5 5
    style User fill:#bfb,stroke:#6f6,stroke-width:2px,color:#000,stroke-dasharray: 5 5
    style TaskManager fill:#9ff,stroke:#369,stroke-width:2px,color:#000,stroke-dasharray: 5 5
    style Status fill:#ffb,stroke:#663,stroke-width:2px,color:#000,stroke-dasharray: 5 5
    style Severity fill:#ffb,stroke:#663,stroke-width:2px,color:#000,stroke-dasharray: 5 5

```

