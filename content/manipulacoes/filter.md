# Filter

Certo, sabemos que o `map` aplica uma função para uma coleção e retorna uma lista dos resultados, mas, imagine se fosse possível *filtrar* uma coleção de acordo com uma condição e retornar ao final uma lista com os itens que são compatíveis?

Essa é a finalidade *principal* do `filter`, por isso, veja o exemplo abaixo para entender um pouco mais sobre:

```clojure
(filter odd? (range 1 21))

;; Resultado:
;;  (1 3 5 7 9 11 13 15 17 19)
```

Temos o `range` que gera uma coleção completa de valores de `1` até `19`, no qual são validados pela função `odd?`, verificando se o número informado é ímpar. Caso seja é adicionado na lista final de retorno, senão é descartado.

O funcionamento quanto ao uso de funções anônimas é idêntico ao `map`, assim, irei adicionar uma demonstração com uma função declarada, por isso, veja o exemplo abaixo:

```clojure
(defn maior-que-3 [n]
  (> n 3))

(filter maior-que-3 (range 1 10))

;; Resultado:
;;  (4 5 6 7 8 9)
```

Assim, podemos facilmente repassar parâmetros e validações a serem realizadas pelo `filter` em específico!

---

E então, curtiu o funcionamento do `filter`? Bem, o que acha de conhecer o `reduce`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/manipulacoes/reduce.md">Próximo -> Reduce</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
