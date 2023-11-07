# Apply

O principal uso do `apply` é no momento de necessidade de aplicação para uma coleção em alguma função, na qual precisamos passar um vetor completo ao invés dos parâmetros puros.

Um exemplo simples utilizando a função `max` (que compara os valores recebidos como argumentos e retorna o maior) está apresentado abaixo:

```clojure
(apply max [1 2 3 4 5]) ;; 5

(max 1 2 3 4 5) ;; 5

;; Função não é aplicada corretamente
;; porque o vetor é visto como um
;; único parâmetro!
(max [1 2 3 4 5]) ;; [1 2 3 4 5]
```

Basicamente poderíamos dizer que o `apply` literalmente *aplica* uma coleção como argumentos para uma determinada função, sendo extremamente útil para outras funcionalidades também!

Sua facilidade é encontrada quando sabemos que podemos retornar um vetor em determinados casos e tratá-lo como uma lista de argumentos e execuções para serem aplicadas.

---

Gostou de conhecer o `apply`? O que acha de partirmos para nosso último tópico: criando um mini servidor HTTP com Clojure?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/projeto/http.md">Próximo -> Mini servidor HTTP</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
