# Vetores

Os vetores podem ser definidos como estruturas sequenciais indexadas, ou seja, possuem índices de identificação. Caso você já tenha tido contato com outras linguagens de programação, provavelmente já se deparou com vetores ou os chamados *arrays* em algum momento.

Não diferente, Clojure implementa os vetores utilizando a notação de colchetes (isso mesmo, nada diferente), na qual podemos definir um vetor de números de forma simples como no exemplo abaixo.

```clojure
[1 2 3 4 5 6 7 8 9]
```
> Não são necessárias vírgulas ou algo do tipo, apenas um espaço entre os itens.

Agora você deve estar se perguntando "ok, mas, você havia me falado que Clojure tratava dados como dados puros certo? Eu consigo ter um vetor com múltiplos tipos?"... Bem, a resposta é sim!

```clojure
[1 2 3 true false "He4rt Developers"]
```
> Múltiplos tipos em uma mesma estrutura não é um problema.

Vamos definir um vetor fixo para trabalharmos e assim realizarmos alguns testes, por isso, sinta-se livre para escolher sobre o que e com quais índices seu vetor deve ter! O meu seguirá o exemplo abaixo:

```clojure
(def desenvolvedores
     ["Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício"])
```

## First

Como poderíamos simplesmente retornar o primeiro índice desse vetor declarado? Simples: utilizando a função `first`!

```clojure
(first desenvolvedores)
```

Nesse caso o output seria `"Kalane"`, afinal, este é o primeiro índice de nosso vetor!

## Rest

E como poderíamos agora mostrar os demais índices, sem contabilizar o primeiro? Isto é, fazer algo semelhante ao `tail` de outras linguagens de programação? Bem, utilizamos neste caso o `rest`!

```clojure
(rest desenvolvedores)
```

Nesse caso o output seria `("Daniel" "Cherry" "Canhassi" "Fabrício")`!

## Nth

Beleza, mas, caso a gente quisesse algum índice específico? Isso seria possível? Claro! Existem ainda duas formas distintas para realizar isso, mas, vou explicar o motivo...

```clojure
(nth desenvolvedores 3)
```
> O output seria `"Canhassi"`!

Ou então poderíamos utilizar simplesmente:

```clojure
(desenvolvedores 3)
```
> O output seria `"Canhassi"`!

A segunda forma perfeitamente por um simples motivo: se lembra quando eu disse que o uso do `def` seria similar ao de se declarar uma função que não recebe argumentos em específico mas possui um retorno? Bem, exatamente neste princípio!

## Count

Para contabilizar a quantidade de valores em nosso vetor podemos utilizar a função `count`!

```clojure
(count desenvolvedores)
```

Nesse caso o output seria `5`, afinal, temos 5 valores em nosso vetor!

## Conj

Podemos ainda concatenar, isto é, adicionar um índice novo em nosso vetor de uma forma muito simples: com a função `conj`!

```clojure
(conj desenvolvedores "Guto")
```

Nesse caso o output seria `["Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício" "Guto"]`, fazendo com que o índice novo seja adicionado ao final do vetor!

## Cons

Para adicionar um elemento no início do conteúdo de um vetor utilizamos a função `cons`!

```clojure
(cons "Guto" desenvolvedores)
```

Nesse caso o output seria `("Guto" "Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício")`!

Agora perceba um ponto específico: nós utilizamos diversas funções que realizam modificações em nosso vetor, imprimindo sempre um valor modificado certo? Mas, vamos ver como fica o valor final de `desenvolvedores` depois de tudo isso...

```clojure
(println desenvolvedores)
```

Bem, ao final você perceberá que a estrutura não foi modificada, permanecendo no valor original de seu momento de declaração! Como falado anteriormente Clojure trata suas estruturas de forma imutável, criando valores novos que podem ser utilizados da forma como você quiser sem modificar a estrutura original, trazendo segurança para seu desenvolvimento!

---

Gostou da forma de tratamento de vetores dentro de Clojure? O que acha de conhecer as listas?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/conceitos/listas.md">Próximo -> Listas</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
