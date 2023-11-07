# Map

Imagine ter uma coleção de valores qualquer e poder aplicar um *efeito* sobre todos os elementos, podendo *mapeá-los* e aplicar uma função específica para todos, retornando ao final uma lista com o resultado?

Para a tarefa citada acima o `map` será seu maior amigo! Veja um exemplo simples abaixo:

```clojure
(map inc [1 2 3 4 5])

;; Resultado:
;;  (2 3 4 5 6)
```

Basicamente aplicamos a função `inc` (que adiciona `1` para cada valor como um contador) em cada um dos elementos da coleção enviada, retornando uma lista ao final.

Poderíamos ainda utilizar funções anônimas para realização de cálculos, como no exemplo abaixo:

```clojure
(map (fn [n] (* n 2)) [1 2 3])

;; Resultado
;;  (2 4 6)
```

Uma outra forma de realizar o mesmo cálculo é não necessariamente *declarando uma função anônima*, mas, utilizando a sintaxe abaixo:

```clojure
(map #(* % 2) [1 2 3])

;; Resultado
;;  (2 4 6)
```

Podemos dizer que o `#` é utilizado para indicar o uso de uma *função anônima*, enquanto o `%` é utilizado para indicar o valor que seria passado como argumento, simplificando ainda mais o processo!

---

O que achou de conhecer o `map`? Vamos dar uma olhada no `filter`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/manipulacoes/filter.md">Próximo -> Filter</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
