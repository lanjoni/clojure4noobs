# Documentações

Ler as documentações de funções específicas em Clojure é algo possível de se realizar dentro do próprio código, utilizando uma simples função chamada `doc`.

## Doc

Com esta função podemos avaliar e ler uma documentação sobre qualquer função que Clojure tenha, com exemplos práticos e uma descrição de funcionamento, facilitando seu desenvolvimento como um todo.

Um exemplo simples seria para a validação da função `+`, que tem como objetivo realizar a soma de valores. Para validar sua documentação podemos executar o código abaixo:

```clojure
(doc +)
```

Assim, será impresso como resposta algo como o trecho abaixo.

```
clojure.core/+
([] [x] [x y] [x y & more])
  Returns the sum of nums. (+) returns 0. Does not auto-promote
  longs, will throw on overflow. See also: +'
nil
```
> Como já falamos anteriormente o `nil` apenas demonstra o retorno final de uma função.

## Find-doc

Bem, agora se você precisa procurar por alguma ação, ou seja, alguma string em específico que esteja presente na documentação mas você não se lembra exatamente a função que realiza esta ação a função `find-doc` vai te auxiliar nesse processo. Veja o exemplo abaixo:

```clojure
(find-doc "sum of nums")
```

O retorno seria algo como:

```
-------------------------
clojure.core/+
([] [x] [x y] [x y & more])
  Returns the sum of nums. (+) returns 0. Does not auto-promote
  longs, will throw on overflow. See also: +'
-------------------------
clojure.core/+'
([] [x] [x y] [x y & more])
  Returns the sum of nums. (+') returns 0. Supports arbitrary precision.
  See also: +
nil
```

Como apresentado, é procurado em toda a documentação de Clojure alguma função que em sua descrição contenha a string enviada como parâmetro.

## Apropos

Bem, se você já tem uma ideia de qual nome sua função tem ou se parece e quer procurar por funções que contenham determinado trecho de texto em seu nome: `apropos` é o nome da função que você está procurando.

Olhe o trecho de código abaixo para procura de funções que contenham determinado nome:

```clojure
(apropos "replace")
```

O retorno apresentado seria algo como:

```
(clojure.core/replace clojure.string/re-quote-replacement clojure.string/replace clojure.string/replace-first clojure.walk/postwalk-replace clojure.walk/prewalk-replace clojure.zip/replace)
```

## ClojureDocs

Caso você prefira uma interface interativa na web, recomendo fortemente utilizar as documentações encontradas no [ClojureDocs](https://clojuredocs.org/), facilitando suas buscas por conteúdos diversos e exemplificações maravilhosas.

---

Então, curtiu entender um pouco sobre o funcionamento de documentações com Clojure? O que acha de passarmos um pouco sobre o funcionamento de estruturas lógicas com Clojure?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/conceitos/logica.md">Próximo -> Lógica</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
