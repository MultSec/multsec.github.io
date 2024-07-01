---
linkTitle: "Configuration"
weight: 3
prev: /docs/multcheck/how_it_works
next: /docs/multcheck/usage
title: Configuration
---

MultCheck relies on a configuration file to define the rules for the checks. The configuration file is a JSON file that contains the following fields:

- `name`: The name of the AV to be used.
- `cmd`: The command to be executed to run the AV scanner.
- `args`: The arguments to be passed to the AV scanner.
- `out`: The output format of a positive detection.

An example configuration file is shown below:

```json
{
  "name": "Windows Defender",
  "cmd": "C:\\ProgramData\\Microsoft\\Windows Defender\\Platform\\4.18.23100.2009-0\\MpCmdRun.exe",
  "args": "-Scan -ScanType 3 -File {{file}} -DisableRemediation -Trace -Level 0x10",
  "out": "Threat information"
}
```

{{< callout type="info" >}}
The `args` field is a string that contains the arguments to be passed to the AV scanner. The `{{file}}` placeholder is used to specify the file to be scanned. The placeholder is replaced with the actual file path during runtime.
{{< /callout >}}

{{< callout type="warning" >}}
Before running MultCheck, ensure that the AV scanner is installed on the system and the path to the AV scanner is correctly specified in the configuration file. A good practice is to test the AV scanner with the specified arguments to ensure that it is working as expected.
{{< /callout >}}