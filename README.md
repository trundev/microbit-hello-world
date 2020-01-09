# Microbit Hello world sample!
Sample project generate by https://ide.mbed.com. It is based on the Mbed repository
[microbit-hello-world](https://os.mbed.com/teams/microbit/code/microbit-hello-world/),
but is modified to use the latest microbit modules from https://github.com/lancaster-university.

## Supported on-line build environments:

### ARM mbed online compiler: https://ide.mbed.com
The Mbed Compiler .lib files are included in branch [master](https://github.com/trundev/microbit-hello-world/tree/master).

***Important!***

The [microbit-dal.lib](https://github.com/trundev/microbit-hello-world/blob/master/microbit-dal.lib) points to
a [microbit-dal](https://github.com/trundev/microbit-dal) repository forked from [original microbit-dal](https://github.com/lancaster-university/microbit-dal).

The HEAD branch [mbed_support](https://github.com/trundev/microbit-dal/tree/mbed_support) includes modifications to allow builing under the ARM-STD toolchain used by the Mbed compiler:
- The use of C++11 features are avoided, esp. in-class initialization of non-static members
- The missing `__end__` symbol is replaced with `Image$$RW_IRAM1$$ZI$$Limit`, this is needed by `MICROBIT_HEAP_ENABLED`

**[All changes](https://github.com/lancaster-university/microbit-dal/compare/602153e...trundev:mbed_support)**


### GitHub Actions: https://github.com/actions
The GitHub workflow YAML file is included in branch [github-workflow](https://github.com/trundev/microbit-hello-world/tree/github-workflow). It uses `ubuntu-latest` virtual machine to install and run `yotta build`.

See: [Supported runners](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/virtual-environments-for-github-hosted-runners#supported-runners-and-hardware-resources)

*The [Actions](https://github.com/trundev/microbit-hello-world/settings/actions) in this repository may be disabled to avoid billing charges*

### Microsoft Azure DevOps Pipelines: https://azure.microsoft.com/en-us/services/devops/pipelines/
The Azure Pipeline YAML files are included in branches:

- [azure-pipelines-linux](https://github.com/trundev/microbit-hello-world/tree/azure-pipelines-linux) - uses `ubuntu-latest` virtual machine
- [azure-pipelines-windows](https://github.com/trundev/microbit-hello-world/tree/azure-pipelines-windows) - uses `windows-latest` virtual machine *(still not working)*

See: [Microsoft-hosted agents](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/hosted)
