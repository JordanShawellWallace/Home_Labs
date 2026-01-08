## Objective
Analyze authentication logs to identify suspicious SSH login activity.

## Environment
- System(s) involved: Ubuntu Linux host
- Log source(s): /var/log/auth.log

## Actions Taken
- Generated multiple failed SSH login attempts using an invalid user
- Reviewed authentication logs for repeated failures

## Key Observations
- Multiple failed SSH authentication attempts were observed
- Attempts targeted an invalid user account
- Activity occurred within a short time window

## Analyst Assessment
The activity is consistent with a brute-force SSH authentication attempt rather than normal user behavior.

## Recommended Actions
- Monitor for continued attempts from the same source
- Implement SSH rate limiting or fail2ban
- Enforce key-based authentication where possible




