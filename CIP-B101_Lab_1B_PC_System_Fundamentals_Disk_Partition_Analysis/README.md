# PC System Fundamentals, Disk Sectors and Partition Analysis

A digital forensics training laboratory (CIP-B101) covering system identification, processes, disk geometry, partition tables, boot processes and file systems, using **safe, read-only** examination methods.

## Scenario

As a junior digital forensic trainee, I carry out a preliminary examination of a computer system that may be involved in an investigation. The work documents hardware and software specifications, identifies potential evidence sources, examines running processes, inspects disk partitions, calculates partition sizes and analyses file systems and boot configurations, without modifying the system or its stored evidence.

## Objectives

- Identify hardware, operating system, storage and memory specifications
- Map potential forensic evidence sources across system layers
- Differentiate programs, processes and threads
- Calculate disk and partition sizes from sector information
- Inspect partition tables with read-only Windows or Linux commands
- Explain the PC boot process and distinguish MBR from GPT
- Identify common file systems and explain their forensic importance
- Produce a professional forensic laboratory report backed by verifiable evidence

## Lab Structure

| Part | Topic |
|------|-------|
| A | System identification and evidence layer mapping |
| B | Program, process and thread investigation |
| C | Disk sector and disk size calculation |
| D | Safe partition table inspection |
| E | MBR, GPT and boot process explanation |
| F | File system identification and interpretation |
| G | Final practical assignment (partitions 1 and 2) |

## Final Task

Identify partitions 1 and 2 from an actual partition table, record their sector information, calculate their sizes in GB, and verify the results against operating system information.

## Key Calculation

```
Size (bytes) = Number of sectors x Sector size (usually 512 bytes)
Size (GB)    = Size (bytes) / 1,000,000,000
Size (GiB)   = Size (bytes) / 1,073,741,824

Sectors in partition = End sector - Start sector + 1
```

## Example Read-Only Commands

**Linux**

```bash
lscpu                 # CPU details
free -h               # memory
lsblk -o NAME,SIZE,TYPE,FSTYPE,MOUNTPOINT
sudo fdisk -l         # partition tables (list only)
sudo parted -l        # partition layout (list only)
blkid                 # file system types
df -hT                # mounted file systems
ps aux                # running processes
```

**Windows (PowerShell)**

```powershell
Get-ComputerInfo
Get-Disk
Get-Partition
Get-Volume
Get-Process
```

## Safety Rules

All disk examinations are **read-only**. Formatting, deleting, resizing or modifying partitions is strictly prohibited. Use list and view options only (for example `fdisk -l`, never `fdisk /dev/sdX` in interactive mode).

## Deliverable

One professionally structured PDF laboratory report containing:

- Calculations
- Screenshots
- System observations
- Explanations
- Conclusions

## Repository Contents

```
.
├── README.md
├── LICENSE
├── Report/          # Final PDF laboratory report
├── Evidence/     # Evidence screenshots
```

## Disclaimer

This repository is for educational purposes only. The laboratory manual and course slides belong to their respective authors and are not included here.

## License

Released under the [MIT License](LICENSE).
