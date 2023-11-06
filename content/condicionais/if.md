# If

O `if` pode ser encontrado em diversas linguagens de programação, sendo que sua principal característica é tomar uma decisão caso uma condição seja verdadeira, ou então, pode seguir por um fluxo alternativo caso não seja verdadeira.

A estrutura do `if` dentro de Clojure é um pouco diferente, afinal, o funcionamento é com funções que recebem parâmetros. Geralmente a estrutura muito conhecida de um `if` seria algo como o exemplo abaixo:

```javascript
if (condicao) {
  // Faça algo
} else {
  // Faça outra coisa
}
```

Bem, em Clojure podemos dizer que o funcionamento é um pouco diferente, por isso, veja o exemplo abaixo:

```clojure
(if (> 1 2)
    (println "1 é maior que 2")
    (println "1 não é maior que 2"))

;; Retorno:
;;  1 não é maior que 2
;;  nil
```

Bem, o funcionamento é bem didático se pararmos para analisar, na qual o `if` segue a estrutura `(if (condicao) (caso positivo) (caso negativo))`, sendo que são enviadas funções internas para tratamento e execução.

Poderíamos ainda ir além, montando o seguinte trecho de código:

```clojure
(def a 5)

(if (< a 0)
    (println "Menor que 0")
    (if (= a 0)
        (println "Igual a 0")
        (println "Maior que 0")))

;; Retorno:
;;  Maior que 0
;;  nil
```

Para facilitar nosso trecho de código podemos ainda utilizar uma *bind* local de valor, o que chamamos de *let*, como no exemplo abaixo:

```clojure
(let [a 5]
  (if (< a 0)
    (println "Menor que 0")
    (if (= a 0)
        (println "Igual a 0")
        (println "Maior que 0"))))

;; Retorno:
;;  Maior que 0
;;  nil
```

Neste caso o *let* é utilizado para relacionar um valor, realizar um *match* de valor com alguma *variável*, podendo ser utilizado dentro do mesmo contexto informado, permanecendo sempre no mesmo escopo que declarado!

Certo, mas, caso eu quisesse executar mais que uma única função em um trecho de código, seria possível? Claro! Para isso utilizamos o `do`, como no exemplo abaixo:

```clojure
(if (> 1 2)
    (do
      (println "Epa, recebi seus valores!")
      (println "Pelo que parece 1 é maior que 2!"))
    (do
      (println "Epa, recebi seus valores aqui hein!")
      (println "Pelo que parece 1 não é maior que 2!")))

;; Retorno:
;;  Epa, recebi seus valores aqui hein!
;;  Pelo que parece 1 não é maior que 2!
;;  nil
```

---

Mas me diz aí, o que achou de conhecer o `if`? Bora conhecer o `when`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/condicionais/when.md">Próximo -> When</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
