# Recursividade

De acordo com José ROmildo Malaquias no Capítulo 6 dos [slides da disciplina de Programação Funcional](http://www.decom.ufop.br/romildo/2012-1/bcc222/slides/06-recursividade.pdf) do Departamento de Computação da Universidade Federal de Ouro Preto, podemos definir que:

> Recursividade é o mecanismo de programação no qual uma definição de função ou de outro objeto refere-se ao próprio objeto sendo definido. Assim função recursiva é uma função que é definida em termos de si mesma.

Podemos dizer de forma *rude* que quando presenciamos *recursividade* presenciamos o ato de uma função invocar uma sub-rotina que neste caso é ela mesma, trazendo um aspecto infinito para algo que é finito (profundo não é mesmo?).

Um exemplo maneiro para recursividade seria contar números de trás pra frente (bem, jaja você vai entender a aplicabilidade disso). Veja o exemplo abaixo:

```clojure
(defn contar [n]
  (println n)
  (if (pos? (dec n))
    (contar (dec n))))

(contar 10)
```

O exemplo acima vai contar de `10` até `1`, retornando `nil` ao final pelo `println`. Temos a entrada de um número sendo impressa na tela, depois, a função `pos?` retorna `true` se o número é maior que `0` (validando se é positivo e maior que `0`), caso seja, chamamos novamente a função `contar` passando o valor de `n - 1` (isso mesmo, `dec` vai reduzir um número de contagem, algo parecido com `i -= 1` em outras linguagens de programação).

Uma outra forma para implementação seria trocar o `contar` pelo `recur`. Veja abaixo:

```clojure
(defn contar-recur [n]
  (println n)
  (if (pos? (dec n))
    (recur (dec n))))

(contar-recur 10)
```

O resultado e funcionamento são os mesmos, mas, o `recur` tem algo interessante para ser dito: ele prepara a função para receber uma chamada recursiva, trabalhando-a de forma mais eficiente sem a necessidade de múltiplos empilhamentos!

Ao executar `(doc recur)` temos a seguinte documentação:

```clojure
-------------------------
recur
  (recur exprs*)
Special Form
  Evaluates the exprs in order, then, in parallel, rebinds
  the bindings of the recursion point to the values of the exprs.
  Execution then jumps back to the recursion point, a loop or fn method.

  Please see http://clojure.org/special_forms#recur
```

---

O que achou de ver um pouco sobre recursividade? Pronto para conhecer os chamamos `multimethods`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/funcoes/multimethods.md">Próximo -> Multimethods</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
