---
linkTitle: "Usage"
weight: 3
prev: /docs/multldr-cli/
title: Usage
---

The MultLdr CLI client is a command-line tool that allows users to interact with the MultLdr server. The MultLdr CLI client provides the following commands:

## help

To get help on the available commands, run the following command:

```shell
$ multldr-cli help
NAME:
   MultLdr CLI client - A new cli application

USAGE:
   MultLdr CLI client [global options] command [command options] 

COMMANDS:
   plugs    Retrieve list of plugins present
   gen      Generates loader with the options provided
   help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --help, -h  show help

$
```

## plugs

The plugs command retrieves the list of plugins present in the system. To get the options for the plugs command, run the following command:

```shell
$ multldr-cli plugs --help
NAME:
   MultLdr CLI client plugs - Retrieve list of plugins present

USAGE:
   MultLdr CLI client plugs [command options]

OPTIONS:
   --server IP, -s IP    Use provided IP for the MultLdr server (default: 127.0.0.1)
   --port PORT, -p PORT  Use provided PORT for the MultLdr server (default: 5000)
   --help, -h            show help
$
```

### Example

{{< video src="plugs.mp4" controls="yes" >}}

## gen

The gen command generates a loader with the options provided. To get the options for the gen command, run the following command:

```shell
$ multldr-cli gen --help
NAME:
   MultLdr CLI client gen - Generates loader with the options provided

USAGE:
   MultLdr CLI client gen [command options]

OPTIONS:
   --server IP, -s IP      Use provided IP for the MultLdr server (default: 127.0.0.1)
   --port PORT, -p PORT    Use provided PORT for the MultLdr server (default: 5000)
   --config FILE, -c FILE  Load configuration from FILE (optional)
   --bin FILE, -b FILE     Use payload binary from FILE
   --help, -h              show help
$
```

### Interactive Mode

The gen command by default runs in interactive mode. In interactive mode, the user is prompted to select the options for the loader. When all the options are selected, the user is prompted if they want to save the configuration to a file and then the loader is generated.

#### Example

{{< video src="gen.mp4" controls="yes" >}}

### Configuration File

The gen command also supports loading the configuration from a file. The configuration file is a JSON file that contains the options for the loader. The configuration file should have the following format:

```json
{
    "execution": [
        "<execution_option_1>",
    ],
    "keying": [
        "<keying_option_1>",
        "<keying_option_2>"
    ],
    "payload_mods": [
        "<payload_mod_option_1>",
        "<payload_mod_option_2>",
        "<payload_mod_option_3>"
    ],
    "post_comp": [
        "<post_comp_option_1>",
        "<post_comp_option_2>"
    ],
    "pre_comp": [
        "<pre_comp_option_1>",
        "<pre_comp_option_2>"
    ]
}
```

The following is an example of a configuration file:

```json
{
    "execution": [
        "/execution/local/FPointer"
    ],
    "keying": [
        "/keying/debug/IsDebuggerPresent1",
        "/keying/sandbox/CPUCycles",
        "/keying/sandbox/Storage"
    ],
    "payload_mods": [
        "/payload_mods/encryption/AES",
        "/payload_mods/encryption/XOR",
        "/payload_mods/encryption/CTAES"
    ],
    "post_comp": [
        "/post_comp/legitemacy/FileBloating",
        "/post_comp/legitemacy/SelfSign"
    ],
    "pre_comp": [
        "/pre_comp/IATHiding/APIHashing",
        "/pre_comp/entropy/WordStuffing"
    ]
}
```

#### Example 
{{< video src="config.mp4" controls="yes" >}}