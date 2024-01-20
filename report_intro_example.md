# PasswordStore Audit Report

Lead Auditors:

-   [Benas Volkovas](https://github.com/BenasVolkovas)

# Table of Contents

- [PasswordStore Audit Report](#passwordstore-audit-report)
- [Table of Contents](#table-of-contents)
- [Disclaimer](#disclaimer)
- [Risk Classification](#risk-classification)
- [Audit Details](#audit-details)
  - [Scope](#scope)
- [Protocol Summary](#protocol-summary)
  - [Roles](#roles)
- [Executive Summary](#executive-summary)
  - [Issues found](#issues-found)
- [Findings](#findings)

# Disclaimer

I make all effort to find as many vulnerabilities in the code in the given time period, but holds no responsibilities for the findings provided in this document. A security audit is not an endorsement of the underlying business or product. The audit was time-boxed and the review of the code was solely on the security aspects of the Solidity implementation of the contracts.

# Risk Classification

|            |        | Impact |        |     |
| ---------- | ------ | ------ | ------ | --- |
|            |        | High   | Medium | Low |
|            | High   | H      | H/M    | M   |
| Likelihood | Medium | H/M    | M      | M/L |
|            | Low    | M      | M/L    | L   |

I use the [CodeHawks](https://docs.codehawks.com/hawks-auditors/how-to-evaluate-a-finding-severity) severity matrix to determine severity. See the documentation for more details.

# Audit Details

The findings described in this document correspond to the following codebase:

-   https://github.com/Cyfrin/3-passwordstore-audit/tree/main

And commit hash:

```
2e8f81e263b3a9d18fab4fb5c46805ffc10a9990
```

## Scope

src/
<br>
--- PasswordStore.sol

# Protocol Summary

PasswordStore is a protocol dedicated to storage and retrieval of a user's passwords. The
protocol is designed to be used by a single user, and is not designed to be used by multiple
users. Only the owner should be able to set and access this password.

## Roles

-   Owner: The user who can set the password and read the password.
-   Outsiders: No one else should be able to set or read the password

# Executive Summary

## Issues found

| Severity          | Number of issues found |
| ----------------- | ---------------------- |
| High              | 2                      |
| Medium            | 0                      |
| Low               | 0                      |
| Info              | 1                      |
| Gas Optimizations | 0                      |
| Total             | 3                      |

# Findings
