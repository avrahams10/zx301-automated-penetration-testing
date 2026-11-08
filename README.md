# ZX301 — Automated Penetration Testing

**Bash-Based Reconnaissance, Credential Assessment and Evidence Reporting**  
**Cybersecurity portfolio case study | Avraham Thomas**

## Overview

I created ZX301 as an **original student-written, menu-driven Bash project** to organize common tasks in an **authorized security-assessment laboratory**. Its workflow combined **Nmap** TCP/UDP reconnaissance, service/script observations, **Searchsploit** reference research, **Netcat** connectivity checks, controlled **Hydra** credential testing, and text/ZIP reporting.

Later **owner-directed, Codex-assisted** revisions added stricter input scope, more cautious result classification, structured output, and clearer failure handling. The school implementation and later versions are separate; neither is described as a production vulnerability scanner or an exploitation framework.

## Assessment workflow

```text
        Authorized target + operator input
                       |
             Bash assessment menu
        Basic / Full / Weak / All / Quit
                       |
         +-------------+-------------+
         |             |             |
      Nmap TCP/UDP  Nmap + NSE   Netcat / Hydra
                     + references
         |             |             |
         +-------------+-------------+
                       |
          Diagnostics, keyword review
                and report / ZIP
```

The original script's documented functions include `get_user_input`, `basic_scan`, `full_scan`, `weak_creds`, and `logging_reporting`. **Searchsploit references are investigation candidates**, not confirmed exploitable vulnerabilities; a script exit or Hydra wrapper message is not independent authentication proof.

## Three distinct evidence streams

| Evidence | Documented result | Qualification |
| --- | --- | --- |
| **Historical student work — August 2025** | Archived school screenshots show menu activity, Nmap observations, candidate references, diagnostic messages, and report packaging | Historical demonstrations, not October 2026 comparisons |
| **Live laboratory comparison — 20 October 2026** | Original and later implementations were run **separately** against the same authorized Metasploitable 2 VM | Supports comparison of recorded tasks, not complete tool equivalence |
| **Reviewer offline regression — October 2026** | Two independently reproduced Linux review runs of **271 mocked checks each**, with **zero reported failures** | Does not validate live credentials, network behavior, exhaustive coverage, or real-world exploitability |

### What the live comparison showed

Both versions recorded **23 confirmed-open Basic TCP entries** and **4 confirmed-open Basic UDP entries**, totaling **27** matching Basic observations per run. `open|filtered` results were not counted as confirmed open. This does **not** demonstrate full service/NSE equivalence or comprehensive vulnerability coverage.

Both runs included **Hydra-reported FTP/SMB success classifications**, but **independent interactive authentication was not confirmed**. SSH/Telnet behavior remained incomplete or unresolved, and the applicability of some Searchsploit references was not established. Neither wrapper completion nor report size is a reliable measure of assessment accuracy.

### What the offline regression showed

The two separately reproduced 271-check runs were performed in different relocated layouts **within one Linux reviewer environment** using mocks and fault injection. The retained logs were byte-identical; independent-run context comes from the review records, not distinct timestamps in the logs. Earlier owner-side or assisted regression claims remain separate evidence and are not counted as these reviewer reproductions.

## Original contribution and later development

- **Original student work:** menu interface; Basic and Full Nmap workflows; Searchsploit lookup; Netcat-gated Hydra checks; search, reporting, and ZIP packaging.
- **Later Phase 1:** more conservative credential-result handling and privacy-aware reports.
- **Later Stages 2A–2D:** input/scope checks, completion status, contextual port parsing, separate run outputs, and storage/write-failure handling.

I developed the original workflow. Later engineering and editorial refinements involved **owner-directed Codex assistance**; the record does not attribute every assisted line to a specific author.

## Lessons, ethical scope and limitations

The project illustrates that **tool output**, **analyst-verified findings**, and **test-harness success** are not interchangeable. All described live assessment activity was limited to approved laboratory targets. No successful exploitation, confirmed compromise, complete scanner equivalence, or production-security improvement is claimed.

## Repository contents

This repository contains a **documentation-only case study**. It does not include runnable scripts, wordlists, credential material, raw Hydra transcripts, internal hosts, original scan archives, historical screenshots, regression bundles, or private reports. Code and additional exhibits require their own exact-version, licensing, ownership, technical, and privacy reviews before release.
