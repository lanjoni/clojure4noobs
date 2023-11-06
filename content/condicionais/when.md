# When

O `if` é uma condicional incrível, afinal, recebe como primeiro argumento uma condição para ser validada, como segundo argumento uma função para ser executada caso a condição seja verdadeira e um terceiro argumento como uma função para ser executada caso a condição não seja verdadeira.

Seria interessante se existisse alguma forma de executar diversas funções de uma vez caso uma condição seja verdadeira, não é mesmo? Bem, para isso que serve o `when`! Veja o exemplo abaixo:

```clojure
(when true
  (println "Testando 1")
  (println "Testando 2")
  (println "Testando 3")
  (println "Testando 4"))

;; Resultado:
;;  Testando 1
;;  Testando 2
;;  Testando 3
;;  Testando 4
;;  nil
```

Sua principal funcionalidade é utilizar de uma condição para executar uma série de funções enviadas! Bem mágico não é?

---

Ok, o `when` realmente é bem maneiro, não é? O que acha de conhecer o `cond` agora?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/condicionais/cond.md">Próximo -> Cond</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
