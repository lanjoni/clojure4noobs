# Doseq

Ok, provavelmente este será o tópico mais curto! O `doseq` é simplesmente um `for` que não retorna nada!

Para entender melhor veja o exemplo abaixo:

```clojure
(def numeros [0 1 2 3 4 5 6 7 8 9])

(doseq [i numeros]
      (println i))

;; Resultado:
;;  1
;;  2
;;  3
;;  4
;;  5
;;  nil
```
> O último retorno (neste caso `nil`) é o valor retornado pelo `doseq`!

Sua utilização é útil quando não precisamos de um retorno em formato de lista ou algo similar como quando utilizamos o `for`!

---

Como eu falei: o `doseq` é bem simples não é mesmo? Bora conhecer nossa última estrutura de repetição, o famoso `loop`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/repeticao/loop.md">Próximo -> Loop</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
