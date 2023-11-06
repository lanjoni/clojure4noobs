# Lógica

Bem, quando falamos de lógica falamos necessariamente de algo a mais: comparação. Como já vimos, o tratamento de funções com Clojure é diferente para todas as funções, trazendo uma sintaxe completamente prefixa.

## =

Começando pelas comparações utilizando a função `=`, temos que:

```clojure
(= 1 true) ;; false

(= 1 1) ;; true

(= true true) ;; true

(= 1 2) ;; false

(= 1 1 1) ;; true

(= 1 1 2) ;; false
```
> Ponto importante: `!=` não existe aqui! Então caso você teste receberá um erro... Continue seguindo os exemplos que vamos repassar o funcionamento de negativas com Clojure!

Pelo que podemos perceber, `true` e `1` não são *nesse caso* tratados como a mesma coisa, implicando no funcionamento geral de algumas comparações! Podemos ainda comparar três valores ou mais, querendo saber se são iguais ou não. Isso é possível graças ao tratamento de sintaxe que foi discutido anteriormente, assim como em outras funções como em `+`.

## > >= < <=

Comparações se valores são maiores e menores é um tanto quanto útil e Clojure deixa ainda mais elegante para você, por isso, vamos ver alguns exemplos abaixo:

```clojure
(< 1 2) ;; true

(<= 1 2) ;; true

(> 1 2) ;; false

(>= 1 2) ;; false

(< 1 2 3) ;; true

(< 1 3 2) ;; false
```

Perceba que ainda assim podemos passar mais de dois parâmetros para a função, sendo que neste caso, no último exemplo, o resultado foi `false` porque não foram passados de forma crescente, ou seja, `1` é menor que `3` mas `3` não é menor que `2`!

## And

Para validar se dois parâmetros são compatíveis podemos utilizar o `and`, que neste caso seria algo parecido com `&&` de outras linguagens de programação. Veja os exemplos abaixo para entender melhor seu funcionamento:

```clojure
(and true true) ;; true

(and true false) ;; false

(and true true true) ;; true
```

Com funcionamento similar aos apresentados anteriormente podemos simplesmente validar se cada um dos parâmetros são verdadeiros, assim, retornando se o resultado final é `true` ou `false`.

## Or

Para validar se um dos parâmetros é compatível podemos utilizar o `or`, que neste caso seria algo parecido com `||` de outras linguagens de programação. Veja os exemplos abaixo para entender melhor seu funcionamento:

```clojure
(or true true) ;; true

(or true false true) ;; true

(or false false) ;; false
```

Neste caso basta um dos parâmetros ser verdadeiro para que o retorno seja `true`, independente da quantidade de argumentos!

## Not

Bem, neste caso o `not` realiza a negativa de alguma condição, que seria algo parecido com `!` de outras linguagens de programação. Veja os exemplos abaixo para entender melhor seu funcionamento:

```clojure
(not false) ;; true

(not true) ;; false

(not (> 1 2)) ;; true
```

No último exemplo sabemos que a função interna `(> 1 2)` por padrão retornaria `false`, afinal, `1` não é maior que `2`, porém, o `not` inverteu este valor e fez com que ao final fosse retornado `true`!

---

O que achou dos tratamentos de lógica com Clojure? Vamos ver sobre o funcionamento de condicionais com Clojure?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/condicionais">Próximo -> Condicionais</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
