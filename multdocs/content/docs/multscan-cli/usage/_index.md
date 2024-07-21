---
linkTitle: "Usage"
weight: 3
prev: /docs/multscan-cli/
title: Usage
---

The MultScan CLI client is a command-line tool that allows users to interact with the MultScan server. The MultScan CLI client provides the following commands:

## help

To get help on the available commands, run the following command:

```shell
$ multscan-cli help
NAME:
   MultScan CLI client - A new cli application

USAGE:
   MultScan CLI client [global options] command [command options] 

COMMANDS:
   machines  Retrieve list of machines present
   scan      Scans the provided executable across the available vms
   help, h   Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --help, -h  show help
$
```

## machines

The machines command retrieves the list of machines present in the MultScan server. To get the options for the machines command, run the following command:

```shell
$ multScan-cli machines --help
NAME:
   MultScan CLI client machines - Retrieve list of machines present

USAGE:
   MultScan CLI client machines [command options]

OPTIONS:
   --server IP, -s IP    Use provided IP for the MultScan server   (default: 127.0.0.1)
   --port PORT, -p PORT  Use provided PORT for the MultScan server (default: 8000)
   --help, -h            show help
$
```

### Example

{{< video src="machines.mp4" controls="yes" >}}

## scan

The scan command scans the provided binary and retrieves the file information and the results of the analysis. To get the options for the scan command, run the following command:

```shell
$ multScan-cli scan --help
NAME:
   MultScan CLI client scan - Scans the provided executable across the available vms

USAGE:
   MultScan CLI client scan [command options]

OPTIONS:
   --server IP, -s IP      Use provided IP for the MultScan server (default: 127.0.0.1)
   --port PORT, -p PORT    Use provided PORT for the MultScan server (default: 8000)
   --sample FILE, -e FILE  Sample file to be scanned FILE
   --help, -h              show help
```


#### Example 
{{< video src="scan.mp4" controls="yes" >}}