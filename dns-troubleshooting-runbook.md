# DNS Troubleshooting Runbook

## Problem

Customer reports that a website or service is unavailable.

## Goal

Determine whether the issue is caused by DNS resolution, incorrect DNS records, server availability, or application failure.

## Initial Questions

- What domain is affected?
- When did the issue start?
- Are all users affected or only some users?
- Was there a recent DNS, hosting, or deployment change?
- What error message does the customer see?

## Troubleshooting Workflow

1. Confirm the reported domain.
2. Check DNS resolution.
3. Verify the domain points to the expected IP address.
4. Check if the issue affects multiple users or locations.
5. Review recent DNS or hosting changes.
6. If DNS looks correct, check server/application status.
7. Escalate if the issue requires infrastructure or engineering access.

## Possible Root Causes

- DNS record points to the wrong IP address.
- DNS record is missing.
- DNS propagation is still in progress.
- Hosting server is unavailable.
- Application is down while DNS is working correctly.

## Customer Response Example

We reviewed the DNS configuration and confirmed that the domain was not resolving to the expected destination. The DNS record has been corrected, and resolution may take time to propagate globally.

We recommend monitoring access over the next 24–48 hours while DNS propagation completes.

## Escalation Criteria

Escalate when:

- DNS records appear correct but the website remains unavailable.
- Server or application logs are required.
- Hosting or infrastructure access is needed.
- The issue affects all users and may represent a service outage.

## Lessons Learned

DNS should be checked early when investigating website or service availability issues.
