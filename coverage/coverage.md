# Coverage

- Requirements
    - lcov package (sudo apt install lcov)
    - Coverage Gutters (VSCode Extensions Marketplace)

To be able to use Coverage Gutters in vscode, we need to modify settings.json file

```json

{
    "coverage-gutters.coverageFileNames": [
        //"lcov.info",
        "cov.xml",
        "coverage.xml",
        "jacoco.xml",
        "coverage.cobertura.xml",
        "*.coverage.lcov"
    ]
}
```

- Command to create lcov file
    - ```cifuzz coverage --format lcov <fuzztarget>```
- Command to create html report (Optional: install Browser in wsl for easy access - See below for install guide for Google Chrome)
    - ```cifuzz coverage <fuzztarget>```


## Install Google Chrome [1]

```shell
cd /tmp
sudo wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb 
sudo apt install --fix-broken -y
sudo dpkg -i google-chrome-stable_current_amd64.deb
```




#### References
[1] https://github.com/microsoft/wslg
