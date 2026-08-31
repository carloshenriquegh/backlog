#review 

Java força o paradigma de orientação a objetos.
Javascript, python são multiparadigmas.
Java é fortemente tipado.
O tipo da variável não muda depois da declaração.

Java é uma linguagem portátil que pode ser executada em diferentes sistemas operacionais (win, lnx) e arquiteturas de computadores (rm64 por exemplo).

O que permite o Java ser independente de compilador

# A base da linguagem java

## 1.1. POO

Paradigma de programação orientada a objetos. A linguagem java gira em torno de classes e objetos para projetar as aplicações, sistemas e lógica do programa. 

Outras linguagens são multiparadigmas como javascript, C++, diferente do java.
## 1.2. Fortemente tipado

Todas as variáveis e expressões são definidas explicitamente qual o tipo da variável, qual o tipo de retorno, qual o tipo de expressão. 

Ao longo da execução do código as variáveis, uma vez declaradas, não podem ser alteradas ao longo do código.

## 1.3. Independente de plataforma

Java é uma linguagem portátil que pode ser executada em diferentes sistemas operacionais (win, lnx) e arquiteturas de computadores (rm64 por exemplo). O programa compilado do java é interpretado por JVM (ambiente de execução que interpreta o bytecode do java)

# 2. JVM

O código java uma vez compilado transforma o código em bytecode que é interpretado pela jvm. O executável é compilado (código para bytecode) e depois interpretado no JVM. Para ser possível interpretar o bytecode é necessário instalar a JVM*.

O JVM garante o isolamento do código.
# 3. Instalação

## 3.1. Ambiente de desenvolvimento VSCode v1.93

1. [Download](https://update.code.visualstudio.com/1.93.1/win32-x64-user/stable) (win) da [versão 1.93](https://code.visualstudio.com/updates/v1_93) do VSCode (compatível com [VSCode minimalista](https://gist.github.com/carloshenriquecrx/8729842e65dcda6974392ddbde0e3389))

## 3.2. Extensões Java para VSCode

Instalar o [*Extension Pack for Java*](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) que contém:

*[Language Support for Java™ by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)*

*[Debugger for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)*

*[Test Runner for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-test)*

*[Maven for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-maven)*

*[Project Manager for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-dependency)*

*[Visual Studio IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)*

### 3.2.1. Configuração do ambiente de desenvolvimento VSCode (Windows) para Java

Instalar o pacote de codificação *Eclipse Adoptium* *[Install the Coding Pack for Java Windows - Eclipse Adoptium](https://aka.ms/vscode-java-installer-win)*

### 3.2.2. Configuração da variável de ambiente para que os comandos sejam reconhecidos no terminal do VSCode

1. Abra o terminal cmd no Windows e entre com os seguintes comandos na ordem:

`pushd C:\`

`for %i in (java.exe) do @echo. %~$PATH:i`

Você deve receber o diretório padrão como retorno:

`C:\Program Files\Eclipse Adoptium\jdk-17.0.14.7-hotspot\bin\java.exe`

Copie o endereço.

2. Pressione o botão Windows e digite "Variáveis de ambiente".

Na janela "Propriedades do sistema" que se abre clique em "Variáveis de ambiente." 

![Variaveis de ambiente windows](variaveis-de-ambiente-windows.png)

No topo da janela que se abre "Variáveis de usuário" clique duas vezes em "*Path*".

Clique em "Novo" cole o endereço que copiamos até o diretório "*bin*". Deve ficar assim:

`C:\Program Files\Eclipse Adoptium\jdk-17.0.14.7-hotspot\bin`

Clique em "*OK*" em todas as janelas abertas até aqui para confirmar a mudança. Feche o VSCode se estiver aberto.

3. Abra um novo terminal no *VSCode* (`CRTL`+`J`).

Execute o comando `java -version`. O comando deve retornar a versão.

# Nome do arquivo e classe pública

O nome da classe tem que ser igual ao nome do arquivo.

Não significa que o arquivo deve conter apenas uma classe.

Deve existir uma classe com o mesmo nome do arquivo com a notação de `public`

```java

puclic class Main {
...
}

class offhand {
...
}

```
# Variáveis 

O Java é fortemente tipado e não permite que o tipo da variável seja trocado ao longo da execução do programa.

```java
public class Main {

  public static void main(String[] args) {
  int minhaIdade = 20;
  minhaIdade = 21;
  minhaIdade = 20;
  minhaIdade = minhaIdade + 1;
  //na linha abaixo o java inferiu que o tipo da variável é string de acordo com o conteúdo definido após o sinal de igual (=)
  var nomeVariavel = "Fernanda"; 
  }
}
```

# Tipos primitivos

```java

public class Main {

  public static void(String[] args) {
  
  //numeros inteiros (mais usados int e long)
  
  // 8 bits -128 a 127
  byte b = 100;
  
  // 16 bits -32.768 a 32.767   
  short s = 10000;

  // 32 bits -2.147.483.648 a 2.147.483.647
  int i = 100000;    
  
  // 64 bits -9.223.372.036.854.775.808 a 9.223.372.036.854.775.807
  long l = 100000L;
  
  //numeros decimais

  // 32 bits precisão simples, fornece poucos numeros pós vírgula
  float f = 10.1f;

  // 64 bits precisão dupla
  double d = 10.01;

  //String (representar palavras e frases)

  //Para textos (não é um tipo primitivo!)
  String meuString = "Textoaqui";
  
  //Representar  apenas um unico caractere
  char meuChar = 'a';
  }
}

```


# Estruturas Condicionais


# Referências

https://www.youtube.com/watch?v=nODe5lFcGpg&list=PLNCSWIsR6ADI_wMAx9F-Iu8Hs9HHxj4sb&index=1