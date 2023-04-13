# Instalação

Bom, se você chegou até aqui, quer dizer que realmente está interessado em dar continuidade nesse aprendizado! Agora vamos instalar e preparar nosso ambiente de desenvolvimento!

## Sistemas operacionais
- [macOS](https://github.com/lanjoni/clojure4noobs/blob/main/content/intro/instalacao.md#macos)
- [Windows](https://github.com/lanjoni/clojure4noobs/blob/main/content/intro/instalacao.md#windows)
- [Linux](https://github.com/lanjoni/clojure4noobs/blob/main/content/intro/instalacao.md#linux)

Teve algum problema com a instalação? Clique [aqui](https://clojure.org/guides/install_clojure) para acessar a documentação oficial de instalação!

> Pré-requisito: já ter instalado Java/JDK! Clique [aqui](https://clojure.org/guides/install_clojure#java) para saber mais.

---

### macOS

A instalação do Clojure para o macOS é feita utilizando o gerenciador de pacotes [Homebrew](https://brew.sh/). Para realizar sua instalação utilize os seguintes comandos no terminal:

```sh
$ brew update
$ brew install clojure/tools/clojure
```

Para instalar uma nova versão do Clojure basta executar:

```sh
$ brew upgrade clojure/tools/clojure
```

Para mais informações sobre a instalação do Clojure no macOS clique [aqui](https://clojure.org/guides/install_clojure#_mac_os_instructions)!

#

### Windows

Para a instalação do ambiente no Windows tenha certeza de que esteja utilizando o `PowerShell 5` ou superior, além do `.NET Core SDK 2.1+` ou `.NET Framework 4.5+`, além de obviamente ter o `Java 8+` instalado.

Assim que tiver estas certezas, basta realizar o download do script clicando [aqui](https://download.clojure.org/install/win-install-1.11.1.1165.ps1).

Assim que você executar o instalador pelo PowerShell, você vai se deparar com uma tela parecida com esta:

```sh
PS Y:\Downloads> .\win-install-1.11.1.1165.ps1
Downloading Clojure tools
WARNING: Clojure will install as a module in your PowerShell module path.

Possible install locations:
  1) \\Drive\Home\Documents\WindowsPowerShell\Modules
  2) C:\Program Files\WindowsPowerShell\Modules
  3) C:\WINDOWS\system32\WindowsPowerShell\v1.0\Modules\
Enter number of preferred install location: 1

Cleaning up existing install
Installing PowerShell module
Removing download
Clojure now installed. Use "clj -h" for help.
```

Para testar, utilize o comando:

```sh
> powershell -command clj 
```

Caso tenha algum problema de instalação, basta clicar [aqui](https://github.com/clojure/tools.deps.alpha/wiki/clj-on-Windows) para acessar o guia oficial!

#

### Linux

As distribuições Linux no geral estão concentradas aqui pois o script de instalação é o mesmo! Caso você esteja utilizando o Homebrew como gerenciador de pacotes, basta utilizar o mesmo comando que o utilizado no macOS! Caso contrário, siga os passos abaixo.

Tenha certeza de que você possui instalado os pacotes `curl` (para realizar requisições em urls), `rlwrap` (para não deixar nenhum "bug" de interface no cli do Clojure) e `Java`. 

O script deixado vai criar um executáveis nos caminhos `/usr/local/bin/clj` e `/usr/local/bin/clojure`, além do diretório `/usr/local/lib/clojure`. Segue o script:

```sh
$ curl -O https://download.clojure.org/install/linux-install-1.11.1.1273.sh
$ chmod +x linux-install-1.11.1.1273.sh
$ sudo ./linux-install-1.11.1.1273.sh
```

Depois de instalado o script `linux-install` pode ser removido. Caso tenha algum problema durante a instalação, basta clicar [aqui](https://clojure.org/guides/install_clojure#_linux_instructions) e seguir o guia oficial!

---

E aí, tudo instalado corretamente? É hora de termos o nosso primeiro contato com a linguagem!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/content/intro/helloworld.md">Próximo -> Hello World!</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs#roadmap">Voltar para o menu principal</a>
</p>
