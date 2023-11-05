# Hello World!

Certo, agora é o momento de nosso primeiro contato com a linguagem de programação Clojure! Obviamente o clássico "Hello World" não ficaria de fora! Por conta disso, abra seu editor de código favorito e vamos para a prática! 

## Exibindo na tela

Agora é o momento de você criar um arquivo com a extensão `.clj`! Eu chamei meu arquivo de `hello_world.clj`... Lembre-se que como Clojure funciona com a famosa JVM, logo, temos contato com praticamente todas as funções do Java (sim, isso significa interoperabilidade)!

Chega de papo e bora pro código, depois a gente vai repassar detalhe por detalhe de funcionamento, por isso, acalme-se! Observe o código abaixo:

```clj
(println "Hello World")
```

Para testarmos, basta abrir o terminal e executar:

```sh
$ clj hello_world.clj
```

Você verá o retorno da mensagem na tela!

## Parênteses

Você percebeu que a sintaxe de Clojure é um pouco diferente do que encontramos no Java, não? Porém a função para imprimir algo chamada `println` possui o mesmo nome, mesmo que não venha com `System.out` anteriormente! 

Por qual motivo a sintaxe é assim? Simples: Clojure utiliza conceitos voltados para Lisp, que possui uma sintaxe extremamente parecida - com notações prefixas - e o característico uso de parênteses!

Ainda vamos entrar com mais detalhes sobre a sintaxe e funcionamento no geral, mas, por agora, não se preocupe! Apenas tenha certeza que tudo funcionou corretamente!

---

Pronto! Agora que você já teve seu primeiro contato com a linguagem de programação Clojure, podemos avançar para os próximos desenvolvimentos! O que você achou?

Caso você queira estudar um pouco mais sobre Lisp, recomendo os materiais da [UFRN](https://www.dca.ufrn.br/~adelardo/lisp/) e [UFG](https://ww2.inf.ufg.br/~eduardo/lp/alunos/lisp/intro.html)!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/intro/leiningen.md">Próximo -> Leiningen</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
