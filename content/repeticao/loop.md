# Loop

Podemos comparar o `loop` como algo parecido quando falamos de `while`, na qual enquanto algo é verdade as instruções continuam sendo executadas!

Veja o exemplo abaixo para observamos melhor:

```clojure
(loop [i 1]
  (when (<= i 10)
    (println i)
    (recur (inc i))))
```

O exemplo acima vai imprimir uma contagem de `1` até `10`, retornando `nil` ao final! A função `inc` é utilizada para incrementar `1` valor em `i`, sendo uma espécie de contador (similar ao que temos como `i += 1` em outras linguagens de programação).

Ao final é necessário utilizar a função `inc`, com finalidade de executar uma expressão em ordem, em formato recursivo, para que assim seja enviado o valor atualizado da *variável* `i`.

Podemos dizer e afirmar que esta é a estrutura básica da estrutura de repetição `loop`!

---

O que achou de conhecer as estruturas de repetição? Qual sua favorita? Vamos estudar um pouco melhor sobre os conceitos por trás de funções em Clojure?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/funcoes">Próximo -> Funções</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
