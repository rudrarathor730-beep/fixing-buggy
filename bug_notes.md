# Bug Notes

| Bug | Cause | Fix |
|---|---|---|
| Incorrect average | Divided by `len(marks) - 1` | Divided by `len(marks)` |
| Single-mark error | Denominator became zero | Corrected the denominator |
| Pass boundary error | Used `mark > PASS_MARK` | Changed to `mark >= PASS_MARK` |
| Wrong grade | Checked lower grades before Distinction | Checked grade thresholds from highest to lowest |

## Conclusion
Unit testing exposed the logic errors. After fixing them, all 9 tests passed.