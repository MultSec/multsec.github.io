---
linkTitle: "Usage"
weight: 3
prev: /docs/multscan/how_it_works
title: Usage
---

When you deploy MultScan, you can access the MultScan UI by navigating to the URL of the MultScan service. The MultScan UI is a web-based interface that allows you to upload an executable sample and retrieve related information about the sample, such as the file type, the file size, the file hash, and the file entropy while also scanning the sample against the configured environments.

To use MultScan, follow these steps:

1. Navigate to the URL of the MultScan service in your web browser.
2. Click the **Choose File** button to upload an executable sample.
3. Click the **Scan** button to retrieve information about the sample and scan the sample against the configured environments.

When you scan a sample, MultScan will run the sample in the configured environments and provide you with the results of the scan. The results of the scan will include the following information:

- The file type of the sample.
- The file size of the sample.
- The file hashes of the sample.
- The public presence of the sample in VirusTotal (other public sources can be added).
- The detection results of the sample in the configured environments.
- The bad bytes being detected in the sample (if byte detection is enabled).

## Example

{{< video src="/demo.mp4" controls="yes" >}}