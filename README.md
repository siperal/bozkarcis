# Siperal Bozkaros CIS RHEL10 Server Level 1/2

Configures a Siperal Bozkaros (RHEL10, Rocky derivative) machine to be CIS compliant.  
These controls **only** supports RHEL family 10.

**Supported Controls:**

1. Server Level 1
2. Server Level 2

This role **will make changes to the system** which may have unintended consequences. This is not an auditing tool but rather a remediation tool to be used after an audit has been conducted.

- Testing is the most important thing you can do.
- Check Mode is not guaranteed!
- This role was developed against a clean install of the Operating System. If you are implementing to an existing system please review this role for any site specific changes that are needed.

## Target System

### Technical Dependencies

- Python 3.8+
- Ansible 2.12+
- python-def
- libselinux-python
- goss binary required for auditing

If you are using the option to create your own bootloader hash the ansible controller

- passlib

## Format

### Conversion Format for NIST References:

1. Standard Prefix:
   - All references are prefixed with "NIST".
2. Standard Types:
   - "800-53" references are formatted as NIST800-53.
   - "800-53r5" references are formatted as NIST800-53R5 (with 'R' capitalized).
   - "800-171" references are formatted as NIST800-171.
3. Details:
   - Section and subsection numbers use periods (.) for numeric separators.
   - Parenthetical elements are separated by underscores (\_), e.g., IA-5(1)(d) becomes IA-5_1_d.
   - Subsection letters (e.g., "b") are appended with an underscore.

## Local Testing

### Example

```bash
molecule test -s default
molecule converge -s wsl -- --check
molecule verify -s localhost
```

## Credits and Thanks

- Original Authors:  
  Mark Bolwell, George Nalen, Steve Williams, Fred Witty
- Forked from:  
  ansible-lockdown
