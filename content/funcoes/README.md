# Funções

Quando falamos de funções falamos da maior parte de tratamento de um ecossistema de linguagens de programação funcionais, na qual *tudo* é *praticamente* uma função. Podemos definir uma função com uma analogia bem simples, dizendo que é uma caixa que espera uma entrada e para esta determinada entrada retorna uma saída, tendo algum tipo de processamento em seu conteúdo interno.

![Exemplo de função Black-Box](https://www.researchgate.net/publication/230646848/figure/fig4/AS:669409437823002@1536611055840/Black-Box-function.png)

Basicamente temos a definição de uma função apresentada acima, mas, como poderíamos declarar uma função em Clojure?

```clojure
(defn oi []
  (println "Oi!"))

(oi)

;; Resultado:
;;  Oi!
;;  nil
```

Basicamente temos uma estrutura formada por:
- `(`: indica o início de uma lista
- `defn`: indica que será declarada uma função
- `[]`: argumentos/parâmetros que essa função recebe (nesse caso nada mesmo)
- `(println "Oi!")`: imprimindo a mensagem "Oi!"
- `)`: indica o fim de uma lista
- `(oi)`: *invocando* a função

As funções como um todo possuem esse formato, no qual é enviado por parâmetro e recebido entre colchetes os valores a serem utilizados dentro da mesma função, assim, podemos declarar uma função simples para somar dois valores:

```clojure
(defn soma [a b]
  (println (+ a b)))

(soma 1 2)

;; Resultado:
;;  3
;;  nil
```
> Lembrando que o `nil` nada mais é do que um retorno do `println`!

Bem, neste formato, poderíamos criar uma função que recebe dois parâmetros e com isso é realizado um cálculo (neste caso de soma) e retornado e apresentado como resultado final.

Certo, mas, caso eu quisesse trabalhar com múltiplos parâmetros, validando cada possibilidade, isso seria possível? Claro! Veja o exemplo abaixo:

```clojure
(defn testando-argumentos
  ([a] (println "Apenas um argumento foi enviado!"))
  ([a b] (println "Dois argumentos foram enviados!")))

(testando-argumentos 1) ;; Apenas um argumento foi enviado!

(testando-argumentos 1 2) ;; Dois argumentos foram enviados!
```

Este caso é bem específico e trata de trabalharmos com funções que possuem tratamentos diferentes de acordo com a quantidade de argumentos recebidos!

Certo, mas, caso tivéssemos a possibilidade de receber infinitos argumentos (assim como a função `+` por exemplo), seria possível? Sim! Veja o exemplo abaixo:

```clojure
(defn infinitos [& args]
  (println args))

(infinitos 1 2 3 4) ;; (1 2 3 4)
```

Neste caso será recebido uma lista de argumentos, dos quais você poderá manipular cada um da forma que desejar! Caso deseje receber apenas o primeiro argumento e ter a possibilidade de receber os demais mas sem a necessidade de tratá-los, saiba que é possível de uma forma bem simples:

```clojure
(defn infinitos-2 [primeiro & args]
  (println "O primeiro argumento foi " primeiro "\nOs demais são: " args))

(infinitos-2 1 2 3 4)

;; Resultado:
;;  O primeiro argumento foi  1 
;;  Os demais são:  (2 3 4)
;;  nil
```

No caso acima tratamos o primeiro argumento apenas, deixando os demais em formato de lista! Caso quiséssemos tratar o segundo também poderíamos adicionar algo como `[primeiro segundo & args]` e assim por diante!

---

Incrível! Agora que já temos a base de como as funções são tratadas em Clojure podemos partir para um tópico um tanto quanto mágico: recursividade!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/funcoes/recursividade.md">Próximo -> Recursividade</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
