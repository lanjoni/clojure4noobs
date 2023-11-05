# Mapas

Os mapas são comumente usados para gerenciar uma associação de chaves a valores, sendo chamado de dicionários ou mapas de hash (famosos hash maps) em outras linguagens de programação.

Podemos dizer que os mapas associam sempre uma chave com um determinado valor, tendo sua sintaxe básica parecida com o exemplo abaixo:

```clojure
{"a" "b" "c" "d"}
```

Quando executado você verá em seu REPL um retorno como `{"a" "b", "c" "d"}`! Perceba que essa vírgula indica a separação interna no mapa que neste caso possui duas chaves com dois valores específicos: chave `"a"` para valor `"b"` e chave `"c"` para valor `"d"`!

Com mapas é normal utilizar vírgulas exatamente por este motivo, mesmo que não obrigatório, ou então separar com uma quebra de linha. Podemos definir um mapa ainda utilizando a função `hash-map`, resultando em algo como o exemplo abaixo:

```clojure
(hash-map "a" "b" "c" "d")
```

O output seria o mesmo! Porém, vamos definir um mapa fixo para utilizarmos em nossos exemplos com a sintaxe abaixo:

```clojure
(def musicas {"Dear Future Self (Hands Up)" "Fall Out Boy"
              "Onlyfans" "Bibi Babydoll"
              "Naquela Mesa" "Nelson Golçalves"
              "Everlong" "Foo Fighters"})
```

## Get

Para selecionar alguma determinada chave e verificar seu valor podemos utilizar duas formas distintas, por isso, vamos começar pela função `get`, veja no exemplo abaixo:

```clojure
(get musicas "Everlong")
```

O output será `"Foo Fighters"`, mas, poderíamos ainda utilizar algo semelhante mostrado anteriormente, apenas informando o nome de um determinado mapa seguido da chave a ser buscada:

```clojure
(musicas "Everlong")
```

O output será o mesmo!

## Assoc

Podemos ainda adicionar novos grupos de chaves e valores em nosso mapa! Para isso utilizamos a função `assoc`, seguido do mapa a ser adicionado, além da chave e do valor específico. Veja o exemplo abaixo:

```clojure
(assoc musicas "Zombie" "The Cranberries")
```

O output seria o mapa completo (separando seus itens com vírgulas) com o novo item adicionado ao final do mapa!

## Dissoc

Podemos ainda remover um item completo identificado pela sua chave utilizando a funçõa `dissoc`! Veja no exemplo abaixo:

```clojure
(dissoc musicas "Dear Future Self (Hands Up)")
```

Assim, seria retornado o mapa completo sem a chave e o valor de `"Dear Future Self (Hands Up)"`!

## Contains?

Validar se um mapa contém uma determinada chave utilizando a função `contains?`! Veja o exemplo abaixo:

```clojure
(contains? musicas "Onlyfans")
```

O output nesse caso seria `true`, mas, caso fosse procurada a chave `"Free Bird"` o retorno seria `false`!

## Find

Além de validar a existência podemos procurar e trazer a chave e o valor específico de um item com a função `find`! Veja no exemplo abaixo:

```clojure
(find musicas "Naquela Mesa")
```

O output nesse caso seria `["Naquela Mesa" "Nelson Golçalves"]`, isso mesmo, em formato de vetor! Caso a chave não existisse seria retornado um `nil` no lugar!

## Keys

Para validarmos todas as chaves de um determinado mapa podemos utilizar a função `keys`! Veja o exemplo abaixo:

```clojure
(keys musicas)
```

O output será `("Dear Future Self (Hands Up)" "Onlyfans" "Naquela Mesa" "Everlong")`, retornando todas as chaves presentes em nosso mapa!

## Vals

Para validarmos todas os valores de um determinado mapa podemos utilizar a função `vals`! Veja o exemplo abaixo:

```clojure
(vals musicas)
```

O output será `("Fall Out Boy" "Bibi Babydoll" "Nelson Golçalves" "Foo Fighters")`, trazendo todos os valores para as chaves existentes!

## Zipmap

Podemos ainda criar um mapa novo a partir de um set específico com a função `zipmap`! Veja o exemplo abaixo:

```clojure
(zipmap #{"a" "b" "c"} (repeat 1))
```

O retorno será `{"a" 1, "b" 1, "c" 1}`, criando um mapa com as chaves originais compondo o set especificado, mas, com valores que surgiram do retorno da função `(repeat 1)`!

## Merge

Combinar mapas é uma tarefa um tanto quanto útil, na qual podemos nos apropriar de diversas finalidades! A função `merge` tem como objetivo combinar dois mapas distintos, trazendo um novo mapa como resultado. Veja o exemplo abaixo com a declaração de um novo mapa:

```clojure
(def novas-musicas {"Sweet Child O' Mine" "Guns N' Roses"
                    "Dream On" "Aerosmith"
                    "Hotel California" "Eagles"
                    "Come As You Are" "Nirvana"})
```

Utilizando a função `merge` temos a seguinte sintaxe:

```clojure
(merge musicas novas-musicas)
```
> Podemos utilizar a função `merge-with` para definir uma regra com objetivo de evitar conflitos caso os mapas tenham chaves iguais!

Neste caso o output será a combinação de todos os valores informados, combinando o primeiro mapa com o segundo!

---

Gostou de ver um pouco mais sobre mapas? Bem, vamos entender um pouco melhor sobre a utilização de documentações com Clojure?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/conceitos/documentacoes.md">Próximo -> Documentações</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
