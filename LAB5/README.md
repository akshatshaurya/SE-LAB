# Lab 5 – Static Code Analysis

**Project:** E-Commerce Cart System  
**Link of forked repository provided in the PDF**  
**Author:** Akshat Shaurya  
**SRN:** PES2UG24CS047  
**Tools Used:** Pylint, Bandit, Flake8  

## Overview
This lab applies static code analysis to a Python E-Commerce Cart System. Three tools were used to find quality, security and style issues in the code without running it, and those issues were then fixed:

| Tool | Checks for |
| :--- | :--- |
| **Pylint** | Code quality, naming conventions, docstrings and likely programming errors |
| **Bandit** | Security vulnerabilities |
| **Flake8** | Code style, formatting and common mistakes |

## Contents

| File | Description |
| :--- | :--- |
| [PES2UG24CS047_Static_Code_Analysis.pdf](PES2UG24CS047_Static_Code_Analysis.pdf) | Lab 5 submission document |

> **Note:** The GitHub link to the forked repository is in the submission document.

## Issues Found & Fixed
- Inconsistent naming conventions and missing docstrings
- Unused imports and variables
- Unsafe use of `eval()`
- Weak MD5 hashing
- Insecure random number generation for PINs
- Shell command execution

The fixes improved naming and documentation, removed unused code, replaced unsafe operations with safer alternatives, and switched to secure functions for PIN generation and hashing.

## Forked Repository Contents
- `ecommerce_cart_system.py`: the corrected Python program
- `issues.md`: table documenting each issue found
- `reflection.md`: answers to the reflection questions
- `reports/`: Pylint, Bandit and Flake8 reports from before and after the fixes
- Git history with separate commits for the Pylint, Bandit and Flake8 fixes
