### Notes for VSC

* Build inside docker for apps:
  * command + shift + p -> config tasks -> build c++ application -> "command": "./docker/docker.sh --build" 
  * docker/docker.sh: docker exec -it $(cat .$DEV_CONTAINER_NAME) make -j 4
  * command + shift + b
  
* Debug inside docker for apps: 
  * [referer](https://medium.com/@spe_/debugging-c-c-programs-remotely-using-visual-studio-code-and-gdbserver-559d3434fb78)
  * install homebrew & gdb: brew install gdb
  * config launch.json:
  ```
      "configurations": [
        {
            "name": "docker gdbserver",
            "type": "cppdbg",
            "request": "launch",
            "program": "${workspaceFolder}/app",
            "miDebuggerServerAddress": "localhost:5555",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": true,
            "MIMode": "gdb",
            "additionalSOLibSearchPath": "${workspaceFolder}/lib",
            "sourceFileMap": {
                "/home/mm/app": "${workspaceFolder}"
            }
        }
    ]
  ```
  * run docker gdb server:  ./docker/docker.sh --gdbserver
  * ./docker/docker.sh: docker exec -it $(cat .$DEV_CONTAINER_NAME) gdbserver :5555 cmd args
  * start debug with breakpoints. (slow)

* Docker with VSC:
  * [referer](https://code.visualstudio.com/docs/azure/docker)
  * run gdb and test through the terminal with vsc
