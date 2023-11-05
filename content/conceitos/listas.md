# Listas

Listas são listas vinculadas sequenciais que, nesse caso, adicionam novos elementos no **início da lista**, em vez de no final, como vetores. Sua sintaxe utiliza parênteses no começo e no final de uma lista.

De fato, como falado anteriormente, todo o nosso código é formado por listas, na qual em grande parte dos casos o primeiro item da lista será uma determinada função. Isso obviamente não é exclusivo do Clojure, mas, um conceito por trás do funcionamento das linguagens de programação da família de Lisp.

## Tratamento

O tratamento de listas é um pouco diferente, por isso, quero que você teste o código abaixo em seu REPL.

```clojure
(1 2 3 4 5)
```

Perceberá que ocorreu um erro, correto? Bem, o motivo é simples: Clojure *pensou* que `1` era uma função e os itens na frente eram nada mais que argumentos para esta determinada função. Para realmente *visualizarmos* essa lista teríamos que adicionar uma aspa simples em seu início, indicando que a lista seguinte não deve ser executada como uma função, prevenindo que ela seja *evaluada* (da tradução literal para avaliada, seria o mesmo conceito que executada - você ainda vai se deparar muito com o termo [evaluation](https://homepages.inf.ed.ac.uk/stg/NOTES/node71.html)).

```clojure
'(1 2 3 4 5)
```

Assim o output será o esperado `(1 2 3 4 5)`. Podemos ainda utilizar a função `list` para a criação de uma lista.

```clojure
(list 1 2 3 4 5)
```
> Esta função declara uma lista que possui como conteúdo os argumentos passados para esta função.

Bem, vamos agora definir uma lista que será utilizada para nossos exemplos abaixo.

```clojure
(def lista-desenvolvedores
    '("Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício"))
```

Assim, podemos utilizar outras funções para manipular esta mesma lista, como por exemplo a função `count`.

```clojure
(count lista-desenvolvedores)
```

O retorno neste caso seria `5`, afinal, temos 5 itens declarados nesta lista!

## First

Como poderíamos simplesmente retornar o primeiro índice dessa lista declarada? Simples: utilizando a função `first`!

```clojure
(first lista-desenvolvedores)
```

Nesse caso o output seria `"Kalane"`, afinal, este é o primeiro índice de nossa lista!

## Rest

E como poderíamos agora mostrar os demais índices, sem contabilizar o primeiro, assim como nos vetores? Bem, utilizamos neste caso o `rest`!

```clojure
(rest lista-desenvolvedores)
```

Nesse caso o output seria `("Daniel" "Cherry" "Canhassi" "Fabrício")`!

## Nth

Beleza, mas, caso a gente quisesse algum índice específico, assim como nos vetores? Isso seria possível? Claro!

```clojure
(nth list-desenvolvedores 3)
```
> O output seria `"Canhassi"`!

Mas, então poderíamos utilizar simplesmente (assim como nos vetores):

```clojure
(list-desenvolvedores 3)
```

Bem, a resposta é não! Se você executou este trecho de código provavelmente se deparou com um erro! Com as listas não podemos trabalhar diretamente com índices como nos vetores...

## Conj

Você se lembra que com vetores podemos adicionar índices no começo e no fim? Bem, com as listas podemos adicionar apenas no começo de toda lista!

```
(conj lista-desenvolvedores "Guto")
```

Neste caso o output seria `("Guto" "Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício")`!

---

O que achou de conhecer um pouco sobre listas? Pronto para entender um pouco melhor sobre sets?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/conceitos/sets.md">Próximo -> Sets</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
