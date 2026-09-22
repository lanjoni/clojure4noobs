# Installation

If you made it this far, you really want to keep going! Let's install Clojure and set up our development environment.

## Operating systems
- [macOS](https://github.com/lanjoni/clojure4noobs/blob/main/content/en/intro/instalacao.md#macos)
- [Windows](https://github.com/lanjoni/clojure4noobs/blob/main/content/en/intro/instalacao.md#windows)
- [Linux](https://github.com/lanjoni/clojure4noobs/blob/main/content/en/intro/instalacao.md#linux)

Had trouble installing? Click [here](https://clojure.org/guides/install_clojure) for the official installation guide!

> Prerequisite: Java/JDK must already be installed! Click [here](https://clojure.org/guides/install_clojure#java) to learn more.

---

### macOS

Clojure on macOS is installed with the [Homebrew](https://brew.sh/) package manager. Run the following commands in the terminal:

```sh
$ brew update
$ brew install clojure/tools/clojure
# or
$ brew install clojure
```

To upgrade to a newer Clojure version, run:

```sh
$ brew upgrade clojure/tools/clojure
# or
$ brew upgrade clojure
```

For more details on installing Clojure on macOS, click [here](https://clojure.org/guides/install_clojure#_mac_os_instructions)!

#

### Windows

On Windows, make sure you have `PowerShell 5` or later, plus `.NET Core SDK 2.1+` or `.NET Framework 4.5+`, and of course `Java 8+` (with the JDK) installed.

Once that is in place, download the installer by clicking [here](https://download.clojure.org/install/win-install-1.11.1.1165.ps1).

When you run the installer from PowerShell, you should see something like this:

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

To try it out, run:

```sh
> powershell -command clj 
```

If you hit installation problems, click [here](https://github.com/clojure/tools.deps.alpha/wiki/clj-on-Windows) for the official Windows guide!

#

### Linux

Linux distros are grouped here because they share the same install script! If you use Homebrew as your package manager, you can use the same command as on macOS. Otherwise, follow the steps below.

Make sure you have `curl` (to download URLs), `rlwrap` (so the Clojure CLI does not glitch when you use the arrow keys), and `Java` (with a full JDK) installed.

The script creates executables at `/usr/local/bin/clj` and `/usr/local/bin/clojure`, plus the directory `/usr/local/lib/clojure`. Here it is:

```sh
$ curl -O https://download.clojure.org/install/linux-install-1.11.1.1273.sh
$ chmod +x linux-install-1.11.1.1273.sh
$ sudo ./linux-install-1.11.1.1273.sh
```

After installing you can delete the `linux-install` script. If anything goes wrong, click [here](https://clojure.org/guides/install_clojure#_linux_instructions) and follow the official Linux guide!

> If you prefer your distro's package manager, look for the `clojure` package!

---

Everything installed? Time for our first contact with the language!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/content/en/intro/helloworld.md">Next -> Hello World!</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
