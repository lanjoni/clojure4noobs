# Multimethods

Este com toda certeza é um dos conceitos mais incríveis para utilização com Clojure! Para entender melhor vamos para um exemplo simples: lembra quando a gente falou sobre o uso de `cond` dentro de nosso código para validar múltiplas condições existentes? Os `multimethods` vão fazer *praticamente a mesma coisa*, porém, de forma muito mais elegante!

Veja um exemplo abaixo para entendermos melhor seu funcionamento:

```clojure
;; Definimos uma identidade, informando
;; que teremos um `multimethod`
(defmulti fatorial identity)

;; Caso a chamada para fatorial tenha
;; como argumento `0`, então, será
;; retornado 1
(defmethod fatorial 0 [_]  1)

;; Caso contrário (:default) será
;; calculado o fatorial de forma
;; recursiva
(defmethod fatorial :default [n]
  (* n (fatorial (dec n))))

(fatorial 0) ;; 1
(fatorial 1) ;; 1
(fatorial 3) ;; 6
```

Neste caso podemos definir de forma mais elegante o formato de tratamento de métodos a serem utilizados dentro de Clojure, calculando apenas quando necessário de forma recursiva (alguns exemplos de implementações para cálculo de fatorial geralmente possuem um `if` para realizar essa validação).

Assim, podemos dizer que o objetivo principal do `defmethod` é deixar de forma clara e compreensiva a declaração de tratamentos para os métodos em específico.

---

Maravilha! Agora que já conseguimos ver sobre `multimethods` podemos passar para um tópico muito interessante: funções anônimas!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/funcoes/funcoes_anonimas.md">Próximo -> Funções Anônimas</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
