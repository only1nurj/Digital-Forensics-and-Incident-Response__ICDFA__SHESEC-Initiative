# Digital Forensics and Incident Response (DFIR)

**ICDFA | SHESEC Initiative**

Parent repository for my Digital Forensics and Incident Response training. It holds my lab reports, notes, scripts and evidence documentation, organised by course module.

## About the Training

This training is delivered by the International Cybersecurity and Digital Forensics Academy (ICDFA) under the SHESEC Initiative. It builds practical skills in digital forensics and incident response through hands-on laboratories, with a focus on safe, verifiable and well-documented investigative work.

## Each module folder follows the same layout:

## Modules

| # | Module | Topics | Status |
|---|--------|--------|--------|
| 01 | PC System Fundamentals, Disk Sectors and Partition Analysis | System identification, processes, sector calculations, MBR vs GPT, boot process, file systems | In progress |
| 02 | To be added | | Planned |

## Working Principles

- **Read-only first:** evidence sources are examined without modification.
- **Document everything:** every finding is backed by a command, screenshot or calculation.
- **Verify results:** calculations are cross-checked against operating system output.
- **Stay reproducible:** commands and steps are recorded so results can be repeated.

## Tools and Environment

- Kali Linux (VirtualBox virtual machine)
- Windows 11 host
- Linux command line, Python 3
- Standard forensic utilities such as `xxd`, `md5sum`, `sha256sum`, `fdisk`, `lsblk`

## Ethics and Safety

All work is done in a controlled training environment on training or personal systems only. No real evidence, third-party data or unauthorised systems are used, and no partitions or disks are formatted, deleted, resized or modified.

## Disclaimer

This repository is for educational purposes only. Course manuals, slides and other materials provided by ICDFA, SHESEC or third parties are not included and remain the property of their respective owners.

## License

The original work in this repository is released under the [MIT License](LICENSE.md).
