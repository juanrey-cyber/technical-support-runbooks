# API Troubleshooting Runbook

## Problem

Customer reports that an API request is failing.

## Goal

Determine whether the issue is caused by authentication, authorization, endpoint configuration, network issues, application errors, or service outages.

## Initial Questions

- What endpoint is failing?
- What error code is returned?
- When did the issue begin?
- Is the issue affecting all requests or specific requests?
- Were any recent changes made?

## Troubleshooting Workflow

1. Confirm the API endpoint.
2. Review the returned HTTP status code.
3. Verify authentication credentials.
4. Verify authorization permissions.
5. Check API documentation.
6. Review logs and request details.
7. Confirm service health and status.
8. Escalate if engineering investigation is required.

## Common Status Codes

- 200 OK
- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found
- 500 Internal Server Error
- 503 Service Unavailable

## Possible Root Causes

- Invalid API credentials.
- Expired token.
- Missing permissions.
- Incorrect endpoint.
- Invalid request format.
- Service outage.
- Application bug.

## Customer Response Example

We reviewed the API request and confirmed the request was being rejected due to an expired authentication token. After generating a new token, requests were processed successfully.

## Escalation Criteria

Escalate when:

- Logs indicate application-side failures.
- Multiple customers are affected.
- Service health issues are detected.
- Engineering access is required.

## Lessons Learned

Authentication, authorization, endpoint validation, and status code analysis should be reviewed before escalation.
