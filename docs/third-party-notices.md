---
layout: default
title: Third-Party Software Notices
permalink: /third-party-notices/
---

# Third-Party Software Notices

> **Pre-release inventory — not the complete release notice.** Generate and include exact copyright and licence texts from the final locked native dependencies before distribution.

**Source baseline reviewed: PressBench v0.17.1, 10 August 2026**

PressBench includes or embeds third-party software and font components. Those components remain owned by their respective copyright holders and are governed by their own licences. Nothing in the PressBench Terms restricts rights granted by an applicable open-source licence.

The reviewed source expressly identifies the following components:

| Component | Identified version or build | Licence noted in source |
|---|---:|---|
| ExcelJS browser bundle | Bundle dated 19 October 2023; exact package version not declared in the embedded header | MIT; includes separately licensed dependencies |
| JSZip | 3.10.1 | MIT or GPL-3.0; PressBench relies on the permissive MIT option |
| jsPDF | 4.2.1, built 17 March 2026 | MIT |
| pako | 2.1.0 | MIT and zlib |
| buffer and safe-buffer browser components | Version not declared in the reviewed header | MIT |
| ieee754 browser component | Version not declared in the reviewed header | BSD-3-Clause |
| Modified Noto font subsets presented as “PressBench Report” | Embedded subsets | SIL Open Font License 1.1 |

The ExcelJS bundle contains additional transitive components and embedded notices. Complete licence headers must remain in the distributed bundle. The final native package should include a generated software-bill-of-materials and complete third-party notice file based on the exact locked dependencies used to build that release.

## Licence sources

- [ExcelJS licence](https://github.com/exceljs/exceljs/blob/master/LICENSE)
- [JSZip licence](https://github.com/Stuk/jszip/blob/main/LICENSE.markdown)
- [jsPDF licence](https://github.com/parallax/jsPDF/blob/master/LICENSE)
- [pako licence](https://github.com/nodeca/pako/blob/master/LICENSE)
- [SIL Open Font License 1.1](https://openfontlicense.org/open-font-license-official-text/)

The embedded Noto subset source contains the complete SIL Open Font License 1.1 text and identifies the font as a modified version. The generated report documents are not themselves required to use the font licence.

For a licensing question, email [lrodeveloperr@gmail.com](mailto:lrodeveloperr@gmail.com?subject=PressBench%20Open%20Source) with the subject **“PressBench Open Source.”**
