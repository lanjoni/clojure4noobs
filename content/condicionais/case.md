# Case

Um pouco diferente do `cond` no formato de tratamento, o `case` busca trazer algo mais próximo do que temos como `switch`/`case` de outras linguagens de programação mesmo, validando casos *inteiros* e destacando um caso adicional para quando nenhum dos demais é contemplado!

Veja o exemplo abaixo e tenho certeza que tudo ficará mais claro!

```clojure
(let [n 10]
  (case n
    1 "Um!"
    2 "Dois!"
    3 "Três!"
    4 "Quatro!"
    "Maior que 4!"))

;; Resultado:
;;  "Maior que 4!"
```
> Nesse caso não utilizamos um `println`, por isso o resultado voltou como uma `string` mesmo!

Com o `case` podemos colocar múltiplos casos e no final adicionar algo que chamamos de `default` em outras linguagens de programação para quando nenhum caso acima foi validado!

---

Maravilha! Chegamos ao final do capítulo e espero que tenha gostado de aprender sobre cada uma das condicionais! Vamos conhecer agora as estruturas de repetição, os famosos *loops*?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/repeticao">Próximo -> Estruturas de Repetição</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
