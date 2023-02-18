# INSTALLAZIONE DI UN NODO MASSA :mechanical_arm:

Note

In questo momento 4 core e 8 GB di RAM dovrebbero essere sufficienti per eseguire un nodo. In futuro questo ammontare di risorse potrebbe non essere sufficiente.
Maggiori informazioni nelle FAQ.

## Installazione utilizzando i files eseguibili binari (installazione semplice)
 

Se vuoi solo eseguire un nodo Massa senza doverlo compilare,  puoi semplicemente scaricare l'ultimo binario qui sotto e andare al passo successivo: 
Eseguire un nodo.

 
[Eseguibile Windows](https://github.com/massalabs/massa/releases/download/TEST.19.3/massa_TEST.19.3_release_windows.zip)

[Eseguibile Linux](https://github.com/massalabs/massa/releases/download/TEST.19.3/massa_TEST.19.3_release_linux.tar.gz)  Funziona solo a partire dalla versione 2.28 di libc (per esempio Ubuntu 20.04 e versioni successive)

[Eseguibile MacOS](https://github.com/massalabs/massa/releases/download/TEST.19.3/massa_TEST.19.3_release_macos.tar.gz)


## Installazione avanzata compilando i files sorgenti


Se si desidera eseguire un nodo Massa dal codice sorgente, ecco i passaggi da seguire:

`rgb(9, 105, 218)` ### Ubuntu / MacOS

Installazione delle librerie necessarie:

su Ubuntu: 
sudo apt install pkg-config curl git build-essential libssl-dev libclang-dev

su MacOS: 
brew install llvm


Installare rustup: 
**curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh**


Configurare la variabile di path: 
**source $HOME/.cargo/env**


controllare la versione di rust: 
rustc --version


installare la versione nigthly: 
rustup toolchain install nightly-2023-01-30


set it as default: 
rustup default nightly-2023-01-30


check rust version: 
rustc --version


clone this repo: 
git clone --branch testnet https://github.com/massalabs/massa.git


### Windows

Set up your Rust environment

On Windows, you should first follow the indications from Microsoft to be able to run on a Rust environment here.
Install Visual Studio (recommended) or the Microsoft C++ Build Tools.
Once Visual Studio is installed, click on C++ Build Tool. Select on the right column called “installation details” the following packages:
MSCV v142 – VS 2019
Windows 10 SDK
C++ CMake tools for Windows
Testing Tools Core Feature
Click install on the bottom right to download and install those packages
Install Chocolatey and run: choco install llvm
Install Rust, to be downloaded here
Install Git for windows, to be downloaded here
Clone the Massa Git Repository

Open Windows Power Shell
Clone the latest distributed version: git clone --branch testnet https://github.com/massalabs/massa.git
Change default Rust to nightly: rustup default nightly-2023-01-30
