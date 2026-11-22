Lab 01: SQLite Ledgers and Conflicting Copies

Name: Abdullah
Roll No: 132251128
Semester: 8
Subject: Introduction to Blockchain

What this lab shows
-------------------
A SQLite database stores 4 certificate events (Issue C-001, Issue C-002,
Revoke C-001, Issue C-003), all approved by the Registrar. The ledger is
exported to week01_ledger.csv. A second copy (Employer) is then changed and
compared with the original. The comparison finds a conflict at event 2:
"Issue certificate C-002" vs "Issue certificate C-999". Both records look
equally valid, so copies alone cannot decide which one is correct.

Files
-----
solution.py       : source code (run in Google Colab)
week01_ledger.csv : Registrar copy
alternate.csv     : Employer copy (event 2 modified)
Screenshots       : Colab output of the code

Output
------
CONFLICT DETECTED: (2, 'Issue certificate C-002', 'Registrar') versus
(2, 'Issue certificate C-999', 'Registrar')

Viva Answers
------------
1. Who can correct the record?
   The authority designated by a documented policy, here the Registrar.

2. Do multiple copies make a blockchain?
   No. There is no hash linking, validation or consensus.

3. When is a registrar database preferable?
   When there is one trusted authority.
