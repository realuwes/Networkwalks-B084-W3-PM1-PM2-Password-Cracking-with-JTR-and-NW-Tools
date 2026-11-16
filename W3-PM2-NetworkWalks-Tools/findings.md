# W3-PM2 - Password Recovery with NetworkWalks Tools

**Student:** Uwes Kulabkar  
**Batch:** B084  
**Execution date:** 16 November 2026  
**Environment:** Windows 11 browser; NetworkWalks Hash Calculator and Password Cracker

## Objective and Scope

Recover the password of the official **PM2-specific** training file `My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf` (**66,735 bytes; approximately 65.2 KiB**). This file is distinct from the larger PDF used for PM1.

## Procedure and Evidence

1. **PDF selection and hash extraction:** In the NetworkWalks Hash Calculator's **PDF** tab, selected the PM2-specific 65.2 KiB training document. The tool identified the file as encrypted and extracted a `$pdf$` recovery value. Evidence: [01 - PM2 hash extraction](Screenshots/4K/01-PM2-NW-Hash-Extraction.png).
2. **Dictionary testing:** Pasted the full recovery value into the NetworkWalks Password Cracker, selected the **built-in list of 100 passwords**, and ran the dictionary test. The interface showed **91 of 100 candidates attempted**, followed by a successful match. Evidence: [02 - password recovered](Screenshots/4K/02-PM2-Dictionary-Password-Recovered.png).
3. **Access verification:** Entered the recovered password into the *same PM2-specific PDF* and verified its completion page. Evidence: [03 - PDF unlocked](Screenshots/4K/03-PM2-PDF-Access-Verified.png).

## Recorded Results

| Field | Observation |
| --- | --- |
| Training file | `My Locked PDF1 (for NW Tools Lab WK3-PM2).pdf` |
| Size | 66,735 bytes / approximately 65.2 KiB |
| PDF hash format | `$pdf$` |
| Reported metadata | Revision R4, Version V4, 128-bit key length |
| Recovery method | NetworkWalks built-in dictionary, 100 passwords |
| Candidates attempted | 91 |
| Password recovered | **`password1`** |
| Access result | Corresponding PM2 PDF opened successfully |

## Interpretation

The password was present in the tested dictionary and was recovered during the controlled exercise. The finding reflects a guessable training password, not an independently verified weakness in the PDF encryption implementation. A stronger, unpredictable password is substantially harder to recover using a small wordlist.

**Recommendation:** Avoid common passwords and password reuse; choose unique long passphrases and protect access to sensitive PDF content.

[Return to project README](../README.md)
