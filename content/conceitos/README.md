# Conceitos

Neste momento vamos entrar em alguns conceitos bem importantes para seu total compreendimento utilizando a linguagem de programação Clojure, na qual um destes conceitos é:

> **Funções** são passageiros de primeira classe, por isso, são tratados de forma exclusiva.

Poderíamos dizer que tudo que temos em Clojure não passam de funções, que combinadas (ou não) resultam em algum dado. Podemos ainda afirmar que em Clojure **dados também são tratados como passageiros de primeira classe**. Dados são dados de forma pura, assim, Clojure não trabalha (e não se importa) diretamente com *tipagem* assim como vemos em outras linguagens de programação.

O intuito de Clojure não é tratar de tópicos relacionados a teoria de tipos ou algo do tipo, mas, ser uma linguagem de programação que trabalha diretamente com dados de maneira pura. Isso é sim um pouco filosófico e é muito do que vemos sendo atribuído e desenvolvido com Clojure.

## Sintaxe

Sim, este momento chegou... O momento de você entender um pouco melhor sobre o funcionamento das sintaxes em Clojure, por isso, abra seu REPL utilizando o comando `lein repl` e bora pra alguns testes!

O primeiro aspecto visual é o uso de parênteses para denotar um início de comando. Basicamente podemos dizer que a sintaxe pode ser simplificada como:

```clj
(funcao argumento1 argumento2 argumento3 ...)
```

Ao abrir os parênteses você *informa* que está começando uma função, nesse caso levando em consideração a sintaxe de Lisp, seria uma lista na qual o primeiro item é o nome da função seguido de seus argumentos, além de implementar tudo que deverá ser feito com aqueles argumentos (como foi apresentado anteriormente).

Um exemplo interessante é a soma, na qual precisamos adicionar o sinal de forma prefixa, não no habituado infixo (na qual o sinal fica entre os argumentos), veja o exemplo:

```clj
user=> (+ 1 2 3 4 5)
15
```

Note que a função foi invocada passando uma lista de argumentos a serem somados! Tecnicamente falando, **sempre** vai ser assim! Simplesmente utilizamos uma função adicionando a quantidade de argumentos que ela espera receber (neste caso esperava uma lista de argumentos sem limite, que somaria todos que fossem adicionados em ordem).

Certo, mas, por qual motivo? Simples: é mais simples. Por mais que seja uma forma nova de se utilizar funções, acredite, é bem mais prático utilizar esse padrão porque você não precisa se preocupar na ordem de nada! É sempre simples: eu adiciono uma função e passo o argumento. Caso o argumento seja outra função, basta simplesmente adicionar um parênteses, como no exemplo abaixo que vou realizar o cálculo matemático `(6 + 2)/2`, olhe:

```clj
user=> (/ (+ 6 2) 2)
4
```

Independente da regra, a sintaxe e ordem é sempre a mesma, criando uma situação em que como tudo são funções é algo relativamente simples de se colocar em prática! Claro, no começo a gente acha estranho mesmo, mas, com o passar do tempo você vai se acostumar!

## "*Variáveis*"

Um tópico bem específico quando falamos de Clojure é sobre variáveis, mas, por qual motivo? Bem, não sei se poderíamos *chamar de variável* algo que não varia. Por padrão, Clojure implementa as váriaveis (apresentadas na documentação oficial no tópico [Vars](https://clojure.org/reference/vars)) como estruturas imutáveis, sendo utilizadas apenas para bindar algum valor em uma determinada palavra-chave (como se fosse uma função que não recebe parâmetros e retorna algo). Porém, para melhor praticidade e seu melhor compreendimento, vamos continuar chamando de variáveis, ok?

As variáveis podem ser definidas utilizando a sintaxe `def` para uma variável, como no seguinte exemplo:

```clj
(def comunidade "He4rt")
```

Agora vamos imprimir uma mensagem utilizando a função `println`, veja:

```clj
user=> (println "Olá" comunidade "!")
Olá He4rt !
nil
```
> Não se preocupe com esse `nil`, afinal, ele só indica que o retorno da função é nulo (pois era uma simples função para imprimir valores). Em Clojure toda função possui um determinado retorno, mesmo que seja `nil`!

Veja, apenas passamos uma lista de argumentos para a função `println` e foi impressa nossa mensagem! Legal não?

---

Eaí, o que achou de entender um pouco mais sobre os conceitos iniciais da linguagem de programação Clojure?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/conceitos/estruturas.md">Próximo -> Estruturas de dados</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
