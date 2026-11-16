# W3-PM1 - Password Recovery with John the Ripper

**Student:** Uwes Kulabkar  
**Batch:** B084  
**Execution date:** 16 November 2026  
**Environment:** Windows 11, John the Ripper with Johnny GUI, browser-based PDF hash extractor

## Objective and Scope

Recover the password of the official institute-provided `My Locked PDF1.pdf` (**273,324 bytes; approximately 266.9 KiB**) using John the Ripper and Johnny. Verify recovery by opening the same PDF and recording its completion page. This is a controlled educational exercise against a supplied training file.

## Procedure and Evidence

1. **PDF preparation:** Selected the larger PM1 training PDF from the institute archive, distinguished from the smaller file intended for PM2.
2. **Extraction:** Used the OnlineHashCrack PDF Hash Extractor to obtain a John-compatible `$pdf$` recovery string. Evidence: [01 - hash extraction](Screenshots/4K/01-PM1-PDF-Hash-Extraction.png).
3. **Local password recovery:** Loaded the PDF recovery data into Johnny (front end for John the Ripper) and completed the password candidate test. Johnny displayed PDF as the hash format and **1/1 cracked**. Evidence: [02 - Johnny recovery](Screenshots/4K/02-PM1-Johnny-Password-Recovered.png).
4. **Access verification:** Opened the PM1 PDF with the recovered password and confirmed that its completion page was displayed. Evidence: [03 - unlocked PM1 PDF](Screenshots/4K/03-PM1-PDF-Access-Verified.png).
5. **Supplementary check:** Re-extracted the hash using the NetworkWalks Hash Calculator and matched it with the browser Password Cracker using an uploaded list of **28 words**. Evidence: [04 - hash cross-check](Screenshots/4K/04-PM1-NW-Hash-Crosscheck.png) and [05 - dictionary cross-check](Screenshots/4K/05-PM1-NW-Dictionary-Crosscheck.png). This was additional practice, **not** a replacement for PM2.

## Recorded Results

| Field | Observation |
| --- | --- |
| Training file | `My Locked PDF1.pdf` |
| Size | 273,324 bytes / approximately 266.9 KiB |
| Recovery format | `$pdf$` (PDF) |
| Primary recovery engine | John the Ripper via Johnny |
| Johnny result | 1 of 1 hashes cracked |
| Password recovered | **`good-luck`** |
| Access result | Corresponding PM1 PDF opened successfully |
| Supplementary browser test | Uploaded wordlist, 28 candidates; `good-luck` matched |

## Interpretation

The result demonstrates that a known-password candidate can be checked against a password-protected PDF without accessing an external service at the time of local John the Ripper recovery. It does not prove a flaw in the underlying PDF encryption. Password strength, rather than encryption-bit length alone, determines resistance to guessing attacks.

**Recommendation:** Use unique, sufficiently long passphrases for sensitive files, protect hash outputs as assessment artifacts, and limit exposure of unlocked documents.

[Return to project README](../README.md)
