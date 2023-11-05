# Leiningen <img align="right" src="https://leiningen.org/img/leiningen.jpg" alt="Imagem da linguagem" width="100">

Leiningen é um gerenciador de dependências com diversas funcionalidades para construção de uma aplicação em Clojure. 

## Como instalar?

Acessando a [página oficial](https://leiningen.org/) você vai se deparar com um script de instalação para qualquer sistema operacional que esteja utilizando. Além disso, você pode instalar utilizando seu gerenciador de pacotes preferidos, como no macOS utilizando o Homebrew.

Por exemplo, utilizando o Homebrew basta executar `brew install leiningen`!

## Utilizando

Para criar um novo projeto utilizando o Leiningen basta executar:

```sh
$ lein new app test
```

> Neste exemplo vamos criar um projeto com o template `app`, mas, ainda existem outros dois templates que podem ser utilizados! Para verificar quais são estas possibilidades basta executar `lein help new`!

Certo, com nosso projeto criado você vai perceber que um diretório surgiu com o nome `test`, ou seja, nosso template foi criado com sucesso. Agora, basta entrar neste diretório e você vai se deparar com uma estrutura parecida com isso:

```md
├── CHANGELOG.md
├── LICENSE
├── README.md
├── doc
│   └── intro.md
├── project.clj
├── resources
├── src
│   └── test
│       └── core.clj
├── target
│   └── test
│       └── stale
│           └── leiningen.core.classpath.extract-native-dependencies
└── test
    └── test
        └── core_test.clj
```

Neste momento podemos verificar alguns arquivos interessantes como o `project.clj` que determina as dependências de nosso projeto, `src/test/core.clj` que seria literalmente o "core" (reconhecido em outras linguagens como o chamado "main" ou "arquivo principal de execução"), além de outros aspectos como geração automática de diretório para testes.

Agora, abra seu arquivo "core" e vamos dar uma olhada no que ele tem para oferecer!

```clj
(ns test.core
  (:gen-class))

(defn -main
  "I don't do a whole lot ... yet."
  [& args]
  (println "Hello, World!"))
```

Perceba que temos a definição de um `main` a ser executado quando executarmos nosso projeto! Para executar basta utilizar `lein run` e será impresso uma mensagem "Hello, World!"! Legal não?

Existem ainda diversas possibilidades ao se utilizar o Leiningen, por isso, durante nosso guia introdutório vamos utilizá-lo sempre que possível!

## REPL

Sim, o Leiningen oferece um "REPL" (Read-Eval-Print Loop) para ser utilizado nativamente em seus projetos, sendo útil para interação direta com uma interface de testes, desenvolvimento com REPL dentre outras finalidades (acredite, sua produtividade e praticidade de desenvolvimento melhoram muito quando você torna o REPL seu amigo)! Para executarmos basta utilizar o comando `lein repl` e você vai se deparar com uma tela parecida com essa:

```sh
nREPL server started on port 49654 on host 127.0.0.1 - nrepl://127.0.0.1:49654
REPL-y 0.5.1, nREPL 1.0.0
Clojure 1.11.1
OpenJDK 64-Bit Server VM 19.0.2
    Docs: (doc function-name-here)
          (find-doc "part-of-name-here")
  Source: (source function-name-here)
 Javadoc: (javadoc java-object-or-class-here)
    Exit: Control+D or (exit) or (quit)
 Results: Stored in vars *1, *2, *3, an exception in *e

test.core=>
```

Utilizando o "REPL" podemos ainda importar funções diretamente de nosso projeto e realizar diversos testes! Ainda conseguimos criar funções e testar possibilidades! Legal não?

---

Excelente! Tivemos nosso primeiro contato com o Leiningen! O que achou? Bora aprender alguns conceitos envolvendo a linguagem de programação Clojure?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/conceitos">Próximo -> Conceitos</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
