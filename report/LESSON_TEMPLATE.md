# Lesson Report Template

Copy this structure into the main report document for each lesson.

## Lesson Number and Title

### Part 1) Goal and Vulnerability Summary

- Vulnerability name:
- Affected component:
- Security impact:
- High-level weakness:

### Part 2) Why This Works / Root Cause

- What trust assumption fails?
- What validation or authorization check is missing?
- Why does the exploit succeed?

### Part 3) Environment and Setup

- DVSA URL / API endpoint:
- AWS region:
- AWS resources involved:
- User/account context:
- Tools used:

### Part 4) Reproduction Steps

1. 
2. 
3. 

### Part 5) Evidence and Proof

- Screenshots:
- Terminal output:
- AWS Console / CloudWatch evidence:
- One short statement that proves the vulnerability:

### Part 6) Fix Strategy / Probable Mitigation

- Where the fix belongs:
- What to change:
- Why the change addresses the root cause:

### Part 7) Code / Config Changes

- File path / Lambda / policy / resource changed:
- Before/after summary:
- Exact snippet or diff reference:

### Part 8) Verification After Fix

- Repeat test:
- Result after fix:
- Legitimate behavior still works:

### Part 9) Structured Operation and Security Analysis

#### Table A

| Vulnerability | Intended Rule(s) | Artifacts Used to Infer Rule | Normal Behavior Evidence | Exploit Behavior Evidence |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

#### Table B

| Vulnerability | Why This Is a Deviation | Deviation Class | Fix Applied (Where) | Post-Fix Verification | Optional Latency Before / After Logging |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

### Part 10) Takeaway / Lessons Learned

- Main security lesson:
- Design principle reinforced:
- One sentence takeaway:
