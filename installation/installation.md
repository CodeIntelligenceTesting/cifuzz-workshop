# cifuzz CLI Installation 


## Windows

#### Setting up Ubuntu (WSL)
 - start Powershell and run ```wsl --install``` or ```wsl --install -d Ubuntu```
 - run ```wsl --update```
 - start Ubuntu and set up your account

#### Setting up cifuzz CLI (WSL)
  - run ```sudo apt update``` and ```sudo apt upgrade```
  - run ```sudo apt install cmake clang llvm lcov gdb zlib1g-dev```
  - run ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/CodeIntelligenceTesting/cifuzz/main/install.sh)"```
  - add to PATH (installation script should provide command e.g. ```echo 'export PATH="$PATH:/home/<username>/.local/bin"' >> ~/.bash_profile```)
  - reload shell ```source ~/.bash_profile```
  - run ```cifuzz --version```
  
  
## macOS

#### Setting up cifuzz CLI (macOS)
  - install homebrew (if not already installed):
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
  - install the dependencies:
  ```bash
  brew install git cmake llvm lcov go openjdk maven gradle bazelisk
  ```

  - add the following to your `~/.zshrc` or `~/.bashrc` to use the correct version of LLVM:
  ```bash
  export PATH=$(brew --prefix)/opt/llvm/bin:$PATH
  export LDFLAGS="-L$(brew --prefix)/opt/llvm/lib"
  export CPPFLAGS="-I$(brew --prefix)/opt/llvm/include"
  ```

  - Install cifuzz:
  ```bash
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/CodeIntelligenceTesting/cifuzz/main/install.sh)"
  ```
  - update your PATH, e.g.
  ```bash
  echo 'export PATH="$PATH:~/.local/bin"' >> ~/.zshrc
  ```
  
  - reload shell ```source ~/.zshrc```
  - run ```cifuzz --version```


## Linux

#### Setting up cifuzz CLI (Linux)
  - run ```sudo apt update``` and ```sudo apt upgrade```
  - run ```sudo apt install cmake clang llvm lcov gdb zlib1g-dev```
  - run ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/CodeIntelligenceTesting/cifuzz/main/install.sh)"```
  - add to PATH (installation script should provide command e.g. ```echo 'export PATH="$PATH:/home/<username>/.local/bin"' >> ~/.bash_profile```)
  - reload shell ```source ~/.bash_profile```
  - run ```cifuzz --version```
