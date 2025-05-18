# WIP
This repo was previously used to store configuration, code, and other files as part of a larger university project.
However, this project is to be transitioned to contain the full working project, including reports and documentation.
As such, it is in the process of being reviewed, cleaned, and updated in a transition from private to public.

## Description
A proof of concept for demonstrating the exploit, detection, and mitigations of CVE-2023-4634.

### CVE-2023-4634 Summary
[CVE-2023-4634](https://nvd.nist.gov/vuln/detail/CVE-2023-4634) is a remote code execution (RCE) vulnerability in the Media Library Assistant (MLA) plugin for WordPress, versions up to and including 3.10.
This vulnerability leverages the Image Tragick vulnerability in the Imagick library used by the MLA plugin.
Polyglot image files are used to bypass input file validation, triggering remote file inclusion, and retrieving a second polyglot image file.
This second file executes a probabalistic local file inclusion attack which can exfiltrate sensitive data and execute remote code.
This vulnerability is executed via remote networks with low complexity, and requires no privileges or user interaction.
As such, it has a 9.8/critical CVSS 3.1 score.

### Acknowledgements and Credits
CVE-2023-4634 was discovered and reported by [Patrowl](https://www.patrowl.io/en/actualites/wordpress-media-library-rce-cve-2023-4634/).
This project was based largely on implementing a functioning copy of the exploit from their work.
