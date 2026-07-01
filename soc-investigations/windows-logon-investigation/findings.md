# Investigation Findings

## Summary

This investigation reviewed Windows authentication events using Event Viewer.

## Key Findings

- Successful logons were identified using Event ID 4624.
- Failed logons were generated and investigated using Event ID 4625.
- Privileged logon activity was reviewed using Event ID 4672.
- Important fields reviewed included account name, logon type, timestamp, failure reason, status code, and computer name.

## SOC Analyst Notes

Repeated failed logons may indicate password guessing, brute-force activity, or password spraying. Privileged logons should be reviewed carefully because they may indicate administrator-level activity.

## Conclusion

This lab helped build foundational SOC skills in Windows log analysis, authentication investigation, evidence collection, and technical documentation.
