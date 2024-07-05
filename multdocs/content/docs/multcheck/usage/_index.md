---
linkTitle: "Usage"
weight: 4
prev: /docs/multcheck/configuration
title: Usage
---

MultCheck accepts a scanner configuration file and a target file as arguments. The scanner configuration file is a JSON file that contains the configuration for the AV engine to be used. The target file is the file that will be scanned.

```bash
$ multcheck -config scanner_config.json <target_file>
```

When the scan is complete, MultCheck will output the scan results to the console. The results will include if the file is clean or infected, and if infected, the bad bytes that are being flagged by the AV engine.

## Example

{{< video src="multcheck_usage.mp4" controls="yes" >}}