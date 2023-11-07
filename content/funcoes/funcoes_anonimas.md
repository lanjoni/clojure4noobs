# Funções Anônimas

Podemos definir uma função anônima como uma função que não necessariamente foi declarada, ou seja, não está vinculada a um identificador qualquer, geralmente podendo *ser passados como argumentos para outras funções*, *utilizadas como um retorno* ou realizar algum tipo de cálculo específico (não vou deixar muitos spoilers sobre os próximos tópicos).

Um exemplo simples de função anônima pode ser definida seguindo o exemplo abaixo:

```clojure
(def ola
  (fn [nome]
    (println "Olá," nome)))

(ola "He4rt Developers")

;; Resultado:
;;  Olá, He4rt Developers
;;  nil
```

A sintaxe para uso de funções anônimas é bem característica, utilizando um `fn` para sua definição, podendo receber parâmetros normalmente (como no exemplo acima), sendo úteis em diversos aspectos.

## Funções que retornam outras funções

Utilizar funções anônimas permite algo mágico: o retorno de outras funções para serem calculadas (eu disse que não iria dar spoiler)!

Olhe o exemplo abaixo e você verá a magia acontecendo:

```clojure
(defn multiplicar [multiplicar-por]
  (fn [n]
    (* n multiplicar-por)))

(def dobrando
  (multiplicar 2))

(dobrando 2) ;; 4

(def triplicando
  (multiplicar 3))

(triplicando 4) ;; 12
```

O funcionamento de uma função anônima neste caso foi para gerar uma nova função para realizar algum tipo de cálculo para multiplicação! Incrível não é mesmo?

---

E aí, o que achou de aprender um pouco mais sobre funções anônimas? Vamos para o tópico de manipulações gerais?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/manipulacoes">Próximo -> Manipulações</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>