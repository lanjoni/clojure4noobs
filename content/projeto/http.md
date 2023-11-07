# Mini servidor HTTP

Neste último tópico vamos criar um simples servidor HTTP passo a passo para você ver como é simples! O objetivo aqui é te apresentar o formato de gerenciamento de projeto com [Leiningen](https://leiningen.org/), apresentando um pouco do mundo de um projeto real!

## Criando seu projeto

Bem, primeiramente crie um projeto com o nome `http-simples`:

```sh
$ lein new app http-simples
```
> O nome `app` é o template esperado! Para entender melhor o funcionamento execute `lein help new`!

Bom, agora que seu projeto está criado a estrutura será similar ao que temos abaixo:

```
.
├── CHANGELOG.md
├── LICENSE
├── README.md
├── doc
│   └── intro.md
├── project.clj
├── resources
├── src
│   └── http_simples
│       └── core.clj
└── test
    └── http_simples
        └── core_test.clj
```

Temos o diretório `test` como um local especial para testes específicos de sua aplicação, `src` para conter todo o código fonte, além de um espaço exclusivo para documentações no caminho `doc`!

Alguns outros pontos como um `README.md`, `LICENSE` (licenciamento de seu projeto) e `CHANGELOG.md` (um formato de *logs* para modificações em versões de seu projeto) também são adicionados.

## Adicionando dependência

Para modificar as definições de seu projeto e neste caso adicionar a dependência do [http-kit](https://github.com/http-kit/http-kit) (um kit para facilmente criarmos um servidor http) precisamos abrir o `project.clj`, na qual sua estrutura será algo como o exemplo abaixo:

```clojure
(defproject http-simples "0.1.0-SNAPSHOT"
  :description "FIXME: write description"
  :url "http://example.com/FIXME"
  :license {:name "EPL-2.0 OR GPL-2.0-or-later WITH Classpath-exception-2.0"
            :url "https://www.eclipse.org/legal/epl-2.0/"}
  :dependencies [[org.clojure/clojure "1.11.1"]]
  :main ^:skip-aot http-simples.core
  :target-path "target/%s"
  :profiles {:uberjar {:aot :all
                       :jvm-opts ["-Dclojure.compiler.direct-linking=true"]}})
```

Para adicionar nossa dependência vamos modificar o trecho com `:dependencies`, assim:

```clojure
;; ...
  :dependencies [[org.clojure/clojure "1.11.1"]
                 [http-kit "2.7.0"]]
;; ...
```
> Estaremos utilizando nessse caso a versão `2.7.0`!

Pronto! Seu projeto já está com as dependências definidas! Para instalar todas as dependências basta executar:

```sh
$ lein deps
```

Maravilha!

## Definindo o servidor

Bem, chegou a hora de definirmos nosso servidor web! Para isso, abra o arquivo `src/http-simples/core.clj`. Nele vamos primeiramente *importar* o `http-kit`, por isso, vamos modificar o namespace:

```clojure
(ns http-simples.core
  (:require [org.httpkit.server :refer [run-server]]))
```
> Esse seria o formato das primeiras duas linhas do projeto!

Agora vamos criar uma função chamada `app` responsável por realizar o redirecionamento de rotas e definição de retornos para cada uma:

```clojure
(defn app [req]
  {:status  200
   :headers {"Content-Type" "text/html"}
   :body    (str "Salve He4rt Developers <3")})
```

Neste caso não importa qual foi o tipo de requisição recebida, não estamos tratando isso! Vamos apenas preparar nosso servidor para receber requisições do tipo GET (por padrão) em nossa raiz do servidor (famosa rota `/`)! No corpo da página deixei uma mensagem, mas, você pode customizar como quiser! Ah, vale ressaltar que é possível modificar também o `"Content-Type"` de acordo com sua necessidade.

Vamos inicializar o servidor em nossa função `main` (famosa função principal) utilizando o `run-server` do `http-kit`, utilizando a função `app` para tratamento de conteúdos acessados!

```clojure
(defn -main [& args]
  (run-server app {:port 3000})
  (println "Server inicializado na porta 3000"))
```

Incrível! Nosso servidor está pronto!

## Executando

Para executar nosso servidor, por favor, volte para a raiz do projeto e execute o seguinte comando:

```sh
lein run
```

E você verá a mensagem que o servidor foi inicializado! Para testar basta abrir seu navegador e acessar `localhost:3000`!

---

Viu como é elegante criar um servidor HTTP com Clojure? Incrível não é mesmo? Vamos para a finalização por agora!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/finalizacao/README.md">Próximo -> Finalização</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
