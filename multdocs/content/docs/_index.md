---
linkTitle: "Documentation"
title: MultSec
---


## What is MultSec?

MultSec is a github organization that aims to provide a multitude of security tools and resources to the public. The aim is to provide a one-stop shop for some security tools and resources while enabling the community to contribute and improve the tools and resources.

## What are the tools and resources provided by MultSec?

The tools and resources provided by MultSec are as follows:

1. [**MultLdr**](https://github.com/MultSec/MultLdr): MultLdr is a modular payload loader generator, that allows you to generate a payload loader that can load multiple payloads in memory. Enabling for a more modular approach to payload loading and execution.

2. [**MultLdr-cli**](https://github.com/MultSec/MultLdr-cli): MultLdr-cli is a command line interface for MultLdr, that allows you save and load configurations for MultLdr. This allows you to easily generate payload loaders with your desired configurations.

3. [**MultCheck**](https://github.com/MultSec/MultCheck): MultCheck is a modular bad bytes checker, that allows you to check for bad bytes in your shellcode against multiple security vendors scanners. This allows you to isolate bad bytes in your shellcode and remove them for better evasion.

4. [**MultScan**](https://github.com/MultSec/MultScan): MultScan is a self hosted multi-scanner that allows you to scan files with multiple security vendors scanners. This allows you to scan files with multiple scanners without having to upload the files to the scanners websites while also enabling you to configure the environment of where they are scanned to better mimic your target environment.

The documentation for each of the tools and resources provided by MultSec can be found below:

<!--more-->

{{< cards >}}
  {{< card link="multldr" title="MultLdr" icon="archive" >}}
  {{< card link="multldr-cli" title="MultLdr-cli" icon="terminal" >}}
  {{< card link="multcheck" title="MultCheck" icon="document-search" >}}
  {{< card link="multscan" title="MultScan" icon="shield-check" >}}
{{< /cards >}}
