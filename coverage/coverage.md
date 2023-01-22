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
- Command to create html report
    - ```cifuzz coverage <fuzztarget>```
