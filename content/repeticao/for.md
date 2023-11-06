# For

Amado por muitos, odiado por alguns, o `for` é um laço de repetição clássico, conhecido na maioria das linguagens de programação por ter um formato um tanto quanto interessante, sendo utilizado muitas das vezes com uma estrutura similar ao que temos abaixo:

```javascript
for (inicializa; até que; passo){
  // Faça algo
}
```
> A estrutura de um `for` varia de acordo com a linguagem de programação obviamente, mas, sempre é interessante ter essa noção de que seu formato não implica necessariamente em sua funcionalidade!

Bem, o `for` em Clojure possui um formato um pouco diferente, por isso, vamos dar uma olhada no exemplo abaixo:

```clojure
(for [i (range 10)]
      (println i))
```

O exemplo acima basicamente vai imprimir os valores de `0` até `9` (dentro do `range` especificado) em uma lista. O `for` em Clojure possui um funcionamento semelhante quando comparado com linguagens de programação que aceitam vetores para tratamento de laços de repetição, por isso, para entender melhor veja mais um exemplo, porém, utilizando um vetor por base:

```clojure
(def numeros [0 1 2 3 4 5 6 7 8 9])

(for [i numeros]
      (println i))
```

No exemplo acima o resultado será igual ao apresentado anteriormente com a função `range`, porém, neste caso foi percorrido todo o vetor existente para atribuir seus determinados valores no laço. Poderíamos utilizar `strings` e ao invés de utilizar o `println` para imprimir uma mensagem, utilizar o `str` para concatenar as strings em uma resposta única, deixando sem aquele retorno ao final. Veja o exemplo abaixo:

```clojure
(def letras ["a" "b" "c" "d" "e"])

(for [l letras]
      (str l))

;; Resultado:
;;  ("a" "b" "c" "d" "e")
```

Uma lista com as determinadas letras é retornada, sendo útil para momentos em que desejamos formar uma nova lista a partir de algum vetor ou algo do tipo... Interessante não é mesmo?

Ainda podemos fazer muito mais com o `for`, por isso, caso tenha interesse recomendo dar uma olhada na documentação do [ClojureDocs](https://clojuredocs.org/clojure.core/for)!

---

Maravilha! Gostou de aprender um pouco mais sobre o funcionamento do `for`? O que acha de conhecermos o `doseq`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/repeticao/doseq.md">Próximo -> Doseq</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
