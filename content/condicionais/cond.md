# Cond

Certo certo, já vimos como seria caso quiséssemos executar um trecho de código grande caso uma condição fosse verdadeira, mas, imagine então validar diversas condições com funções específicas para cada uma?

Bem, vamos conhecer o `cond` com um exemplo bem simples: validando múltiplas condições...

```clojure
(let [n 10]
  (cond
    (> n 0) (println "O número é positivo!")
    (< n 0) (println "O número é negativo!")
    :else (println "Ok, o número não é positivo nem negativo...")))

;; Resultado:
;;  O número é positivo!
;;  nil
```

Basicamente com o `cond` podemos executar múltiplas funções para validações, podendo trabalhar de forma simples com condições complexas! O único detalhe é para o `:else`, que sempre deve cair como uma última condição de caso, na qual nenhuma das demais foi satisfeita!

---

Utilizar o `cond` em seus projetos é um tanto quanto útil, correto? Vamos conhecer a nossa última condicional do capítulo (nada mais nada menos que `case`)?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/condicionais/case.md">Próximo -> Case</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
