# Introdução <img align="right" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/clojure/clojure-original.svg" alt="Imagem da linguagem" width="100">

## O que é Clojure?

### História

Clojure é uma linguagem de programação criada em 2007 por [Rich Hickey](https://github.com/richhickey), com dialetos da família de linguages de programação Lisp utilizando funções como estruturas de dados elementares, com conceitos envolvendo imutatibilidade de dados, sendo executada na Máquina Virtual Java (famosa JVM), mas, podendo ainda ser executada em outros ambientes, tais como o Clojure CLR (compilando o código para .NET) além de ClojureScript (que compila o código para JavaScript).

- **Certo, mas, de onde veio essa ideia?**

Antes de começar a desenvolver a linguagem de programação Clojure, Rich trabalhou na *dotLisp* com um projeto muito semelhante para a plataforma .NET, além de desenvolver a interface **jfli** (uma ponte de recursos do Java para Common Lisp), **FOIL** (uma interface de objetos externos para Lisp) e **Lisplets** (uma interface amigável do Lisp para Java Servlets), criando aspectos de interoperabilidade entre Lisp e Java.

Levando aproximadamente 2 anos de foco total trabalhando no desenvolvimento da linguagem de programação Clojure, Rich finalmente poderia publicar um anúncio da linguagem para a comunidade Common Lisp.

### Filosofia

O principal objetivo de criação da linguagem foi construir uma versão moderna da linguagem Lisp para a programação funcional, sendo executada na JVM e desenhada para computação concorrente.

Podemos dizer que em Lisp como um todo, não diferente em Clojure, tudo possui formato de uma lista, na qual o primeiro item sempre será a *função*, seguido dos seus argumentos em específico, determinando ações a serem executadas.

Um ponto importante para se relacionar com Clojure é que seu objetivo é ser uma linguagem de programação estável, trazendo um ambiente pronto para produção, na qual a utilização da JVM é um bônus com questões adicionais relacionados ao gerenciamento de uma máquina virtual como um todo.

No artigo [A History of Clojure](https://dl.acm.org/doi/pdf/10.1145/3386321), Rich Hickey demonstra uma série de aspectos relacionados a Clojure, demonstrando mais do que tudo sua estabilidade quanto a linhas de código.

![Linhas de código em Clojure](https://github.com/lanjoni/clojure4noobs/blob/main/.github/clojure_lines_of_code.png)

No exemplo acima podemos notar a estabilidade com linhas de código em determinado ano, demonstrando que uma aplicação Clojure construída em uma determinada versão funcionará *praticamente* perfeitamente 10 anos depois sem muitos problemas em uma versão mais atualizada.

## Onde podemos ver Clojure?

Sendo utilizada por diversas empresas como Walmart, Accenture, Mercado Livre, SoundCloud e Puppet Labs, o suporte fornecido é feito pela Cognitect, que atualmente faz parte do grupo Nubank (sim, a Nubank utiliza Clojure)! 

A primeira versão pública de Clojure surgiu em 2007, enquanto a primeira versão estável surgiu em 2009. Atualmente estamos na versão 1.11.1 (do dia 5 de abril de 2022)!

---

E aí? Gostou da linguagem Clojure? O que acha de realizarmos sua "instalação" e começarmos nossos primeiros testes?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/content/intro/instalacao.md">Próximo -> Instalação</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
