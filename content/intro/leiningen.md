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

Perceba 
