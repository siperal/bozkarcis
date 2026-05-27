# Bozkarcis Audit with Goss

## Overview

Based on BozkarCIS 1.0.1 - 13-Jul-2026

Ability to audit a system using a lightweight binary to check the current state.

### Memory Usage

- ~ 11 MB
- Lightweight
- Self-contained

It works using a set of configuration files and directories to audit CIS of RHEL family 10 servers. These files/directories correlate to the CIS Level and STIG_ID

Tested on

- Siperal Bozkaros Server 1.0 (Ergenekon)

## Requirements

You must have [goss](https://github.com/goss-org/goss/) available to your host you would like to test.

You must have sudo/root access to the system as some commands require privilege information.
