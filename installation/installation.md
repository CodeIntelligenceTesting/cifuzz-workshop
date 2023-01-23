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


## Linux

#### Setting up cifuzz CLI (Linux)
  - run ```sudo apt update``` and ```sudo apt upgrade```
  - run ```sudo apt install cmake clang llvm lcov gdb zlib1g-dev```
  - run ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/CodeIntelligenceTesting/cifuzz/main/install.sh)"```
  - add to PATH (installation script should provide command e.g. ```echo 'export PATH="$PATH:/home/<username>/.local/bin"' >> ~/.bash_profile```)
  - reload shell ```source ~/.bash_profile```
  - run ```cifuzz --version```
