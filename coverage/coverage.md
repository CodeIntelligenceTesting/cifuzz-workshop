# Coverage

To be able to use coverage gutter in vscode, we need to modify settings.json file

```json

{
    "python.defaultInterpreterPath": "/usr/bin/python3",
    "files.autoSave": "afterDelay",
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
