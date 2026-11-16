# Lab 7 – Fuzz Testing for Input Validation Bugs

**Project:** Warranty Claims Application  
**Author:** Akshat Shaurya  
**SRN:** PES2UG24CS047  
**Tools Used:** Python 3.13.7, pytest 9.2.0, Hypothesis 6.170.14  

> [!IMPORTANT]
> ### 🔗 Forked Repository
> The link to the forked GitHub repository is in the PDF.

## Objective
This lab uses property-based fuzz testing with the Hypothesis library to find input-validation bugs in the Warranty Claims application. The application was then hardened to handle malformed or unexpected input safely.

## Contents

| File | Description |
| :--- | :--- |
| [PES2UG24CS047_LAB7_SE.pdf](PES2UG24CS047_LAB7_SE.pdf) | Lab 7 report with execution and test evidence |

## Functions Tested

| Function | Input | Validation added |
| :--- | :--- | :--- |
| `parse_claim` | `plan:age-in-months` | Requires the `:` separator, a non-empty plan name, and a finite, non-negative month value |
| `age_average` | Comma-separated ages | Requires a non-empty list of valid, non-negative integers |
| `payable_charge` | `charge\|discount` | Requires the `\|` separator and two finite, non-negative numbers |

Invalid input now raises a `ValueError` with a clear message. The command-line interface catches it and prints the message instead of crashing with a traceback.

## Results

| Stage | Outcome |
| :--- | :--- |
| Original application, input 25 | Crashed: `ValueError: not enough values to unpack (expected 2, got 1)` |
| Tests on the original code | 6 failed, 3 passed |
| Corrected application, input 25 | Shows a validation message and carries on |
| Final test run | 9 / 9 passed (2.86 s) |

Examples from the corrected application: the ages `12,24,36` give an average of `24`, and the charge `1500|200` gives a payable amount of `1570.0`.

## How the tests were designed
- Hypothesis generates text, None, integers, floats and booleans to try unexpected input types and edge cases.
- Valid generated inputs check that normal behaviour still gives the right result.
- Explicit malformed cases cover a missing separator, an empty age list and a missing discount.

## What the report covers
- Objective
- Environment and project files
- Running the original application
- Hypothesis test design
- Running the tests against the original code
- Fixing input validation
- Running the corrected application
- Final Hypothesis test run
- Updating the GitHub repository
- Deliverables
- Conclusion

## Running the Tests
```bash
pip install pytest hypothesis
python -m pytest test_warranty_claims.py -v
```
