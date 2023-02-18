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

### Ubuntu / MacOS

Installazione delle librerie necessarie su Ubuntu: 
```sudo apt install pkg-config curl git build-essential libssl-dev libclang-dev```

Installazione delle librerie necessarie su MacOS: 
```brew install llvm```

Installare rustup: 
```curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh```

Configurare la variabile di path: 
```source $HOME/.cargo/env```

controllare la versione di rust: 
```rustc --version```

installare la versione nigthly: 
```rustup toolchain install nightly-2023-01-30```

configurare la versione nightly come default: 
```rustup default nightly-2023-01-30```

controllare la verione di rust: 
```rustc --version```

clonare il repository di MASSA: 
```git clone --branch testnet https://github.com/massalabs/massa.git```


### Windows

#### Configurare l'ambiente Rust

Come prima indicazione, devi seguire le [istruzioni di Microsoft](https://docs.microsoft.com/en-gb/windows/dev-environment/rust/setup) per configurare un ambiente RUST.

Installare Visual Studio (raccomandato) oppure i Microsoft C++ Build Tools.

Una volta che Visual Studio è installato, cliccare su C++ Build Tool. 

Nella colonna di destra denominata “installation details” selezionare i seguenti pacchetti: 

+ MSCV v142 – VS 2019
+ Windows 10 SDK
+ C++ CMake tools for Windows
+ Testing Tools Core Feature

Fai clic su installa in basso a destra per scaricare e installare questi pacchetti

Installare Chocolatey ed eseguirlo: 
```choco install llvm```

Installare Rust, scaricandolo da [qui](https://www.rust-lang.org/tools/install)  

Installare Git for windows,scaricandolo da [qui](https://git-scm.com/download/win)

#### Clonare il repository Git di MASSA

Eseguire Windows Power Shell

Clonare l'ultima versione distribuita: 
```git clone --branch testnet https://github.com/massalabs/massa.git```

Configurare l'esecuzione della versione nightly di Rust come default: 
```rustup default nightly-2023-01-30```
