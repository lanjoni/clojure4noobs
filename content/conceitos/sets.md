# Sets

Sets, da tradução literal como *conjuntos* (sim, eu preferi não traduzir para não ficar algo tão diferente do que conhecemos em outros locais). Os sets são como conjuntos matemáticos – não ordenados e sem duplicatas, sendo ideais para verificar com eficiência se uma coleção contém um elemento ou para remover qualquer elemento arbitrário.

Para definir um set podemos utilizar o exemplo abaixo:

```clojure
#{1 2 3 4 5}
```

O output será o mesmo que o enviado, você pode notar que sets também não aceitam que um item seja duplicado! Assim, se você enviar algo como `#{1 2 3 4 5 1}` perceberá que um erro ocorrerá, informando que a chave `1` está duplicada!

Vamos definir um set para utilizarmos em nossos próximos exemplos, veja abaixo:

```clojure
(def set-desenvolvedores
    #{"Kalane" "Daniel" "Cherry" "Canhassi" "Fabrício"})
```

## Set?

Para validar se algo é realmente um set podemos utilizar a função `set?`! Veja o exemplo abaixo:

```clojure
(set? desenvolvedores)
```

O output será `true`, afinal realmente é um set! Agora se executarmos `(set? lista-desenvolvedores)` será retornado um `false`!

## Contains?

Bem, para validar se algum valor existe dentro de um determinado set podemos utilizar duas formas, começando pela função `contains?`!

```clojure
(contains? set-desenvolvedores "Daniel")
```

O output será `true`, afinal, realmente temos o valor `"Daniel"` no set! Mas, se executarmos `(contains? set-desenvolvedores "Guto")` perceberemos que o output será `false`!

Bem, ainda podemos realizar a verificação de outra forma, como no exemplo abaixo:

```clojure
(set-desenvolvedores "Daniel")
```

O output nesse caso será `"Daniel"`, e caso execute `(set-desenvolvedores "Guto")` perceberá que o output é `nil`! Mas, por qual motivo isto funciona?

Bem, se lembra quando eu falei que os sets eram uma coleção de hashs? Teoricamente o valor passado é a chave, no caso do set, quando encontrado ele a retorna (que seria como um valor realmente), mas, quando não encontra retorna nulo!

## Keywords

Podemos ainda declarar um set de keywords, com a sintaxe `:keyword`! Seu valor é sua própria declaração, por isso, possui algumas propriedades diferentes de quando trabalhamos com strings...

Se você tentar executar algo como `("Guto" set-desenvolvedores)` não verá mais um `nil`, mas, verificará que um erro ocorreu! Com `keywords` isso não ocorre, na qual podemos utilizar o keyword a ser validado tanto antes quanto depois de um set, como no exemplo abaixo:

```clojure
(def letras #{:a :b :c})

(:a letras) ;; :a

(letras :a) ;; :a

(:d letras) ;; nil
```

## Conj

Podemos ainda utilizar o `conj` para adicionar um novo item ao nosso set, como no exemplo abaixo:

```clojure
(conj set-desenvolvedores "Guto")
```

O output será `#{"Canhassi" "Kalane" "Daniel" "Fabrício" "Guto" "Cherry"}`, com nosso set contendo o valor especificado!

## Disj

Para remover algum índice de nosso set podemos utilizar a função `disj` como no exemplo abaixo:

```clojure
(disj set-desenvolvedores "Fabrício")
```

O output será `#{"Canhassi" "Kalane" "Daniel" "Cherry"}`, removendo o valor especificado! Caso o valor não exista será retornado o set normalmente, sem alertar nenhum erro ou algo do tipo, tratando normalmente.

---

O que achou dos sets dentro de Clojure? Vamos dar uma olhada nos mapas?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/conceitos/mapas.md">Próximo -> Mapas</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
