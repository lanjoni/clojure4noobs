# Reduce

Imagine poder mapear uma coleção e retornar um único resultado, sendo este o resultado aplicado para o conjunto completo de forma *encadeada*?

Parece um pouco complexo mas garanto que é prático de se utilizar, por isso, veja o exemplo abaixo:

```clojure
(reduce + [1 2 3 4])

;; Resultado:
;;  10
```

Basicamente o `reduce` foi aplicado na sequência apresentada, simplificando algo como `(+ 4 (+ 3 (+ 1 2)))`!

Um outro exemplo, mas, agora utilizando uma função seria:

```clojure
(defn multiplicar [a b]
  (* a b))

(reduce multiplicar [1 2 3 4])

;; Resultado:
;;  24
```

O funcionamento foi seguindo o formato anterior, porém, com uma função em específico. Poderíamos decompor como: `1 * 2 = 2` -> `2 * 3 = 6` -> `6 * 4 = 24`! Sua utilização é baseada na aplicação completa em uma coleção.

---

O que achou do `reduce`? Prático não é mesmo? Vamos conhecer o `apply`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/manipulacoes/apply.md">Próximo -> Apply</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
