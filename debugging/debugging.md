# Debugging in Visual Studio Code

After your fuzz targets were build you need to create .vscode/launch.json with the following content:

```json
{
    "version": "0.2.0",
    "configurations": [        
        {
            "name": "Debug fuzz_EXAMPLE",
            "type": "cppdbg",
            "request": "launch",
            "program": "${workspaceFolder}/.cifuzz-build/libfuzzer/address+undefined/fuzz_EXAMPLE",
            "args": [
                "-timeout=0",
                ".cifuzz-corpus/fuzz_EXAMPLE"
            ],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [
                {
                    "name": "ASAN_OPTIONS",
                    "value": "halt_on_error=0"
                },
                {
                    "name": "NO_CIFUZZ",
                    "value": "1"
                },
            ],
            "externalConsole": false,
            "MIMode": "gdb",
            "setupCommands": [
                {
                    "description": "Enable pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ],
            "miDebuggerPath": "/usr/bin/gdb"
        }
    ]
}
```