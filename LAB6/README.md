# Lab 6 – Code and Branch Coverage Analysis

**Project:** Warranty Claims  
**Author:** Akshat Shaurya  
**SRN:** PES2UG24CS047  
**Tools Used:** pytest, coverage.py  

> [!IMPORTANT]
> ### 🔗 Forked Repository
> The link to the forked GitHub repository is in the PDF.

## Objective
The goal of this lab was to measure and improve code (line) coverage and branch coverage for the Warranty Claims Python application by adding test cases to the provided test file.

## Contents

| File | Description |
| :--- | :--- |
| [PES2UG24CS047_Lab6.pdf](PES2UG24CS047_Lab6.pdf) | Lab 6 report: coverage results, commits and the forked repository link |

## Results

**Coverage of `warranty_claims.py`:**

| Metric | Before (2 tests) | After (22 tests) |
| :--- | :--- | :--- |
| **Line coverage** | 38% | 100% |
| **Branch coverage** | 32% | 100% (26/26 branches) |

*All 22 tests pass.*

## What the new tests cover
- **Input validation:** unknown plans, invalid age
- **Warranty and registration:** within warranty, registered standard plan, premium registration with no extra coverage
- **Claim types:** normal, accidental, excess above 12 months, accidental claims above 12 months
- **Claim limits:** recall and normal claims, both allowed and over the limit, plus claims within 30 days
- **Status and priority:** hardware and software claims at each status (on track, at risk, critical), plus hardware and software priority

## What the report covers
- **Objective**
- **Code Coverage Analysis:** line coverage before and after the new tests
- **Branch Coverage Analysis:** tests that cover both outcomes of every decision
- **GitHub Commits:** commit history pushed to the fork
- **Repository Link:** the forked repository

## Commands Used
```bash
python -m coverage run -m pytest -v CodeCoverageTest_warranty_claims.py
python -m coverage run --branch -m pytest -v BranchCoverageTest_warranty_claims.py
python -m coverage report -m
```
