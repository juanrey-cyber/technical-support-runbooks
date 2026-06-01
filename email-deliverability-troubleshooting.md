# Email Deliverability Troubleshooting Runbook

## Problem

Customer reports that emails are going to spam, being rejected, or not arriving at all.

## Goal

Identify the root cause and restore successful email delivery.

## Initial Information to Gather

- Affected domain
- Email provider
- Error messages received
- When the issue started
- Whether all users are affected

## Investigation Process

### Troubleshooting Workflow

When a customer reports email delivery issues, I would avoid making assumptions and follow a structured process:

1. Confirm the scope of the issue.
2. Identify the affected domain and email provider.
3. Review any bounce-back or error messages.
4. Check DNS records related to email delivery.
5. Validate SPF, DKIM, and DMARC configuration.
6. Identify the most likely root cause.
7. Apply or recommend the fix.
8. Monitor results after DNS propagation.
   
### Step 1 - Verify DNS Records

Check:

- MX records
- SPF records
- DKIM records
- DMARC records

### Step 2 - Review SPF

Confirm that authorized mail servers are allowed to send email on behalf of the domain.

### Step 3 - Review DKIM

Confirm that messages are cryptographically signed by authorized systems.

### Step 4 - Review DMARC

Confirm that DMARC policy is configured correctly and aligns with SPF and DKIM.

## Root Cause Analysis

Determine which configuration is causing delivery failure.

## Resolution

Implement the required DNS or email authentication correction.

## Validation

## Customer Response Example

We identified an email authentication configuration issue affecting message delivery.

The affected DNS records were reviewed and the necessary corrections were applied. Because DNS changes require propagation time, full resolution may take up to 24–48 hours.

We recommend monitoring delivery results during this period and contacting support if any additional failures occur.

Confirm successful delivery after DNS propagation and testing.

## Escalation Criteria

Escalate the issue when:

- DNS records appear correct but delivery failures continue.
- The issue involves provider-side outages.
- Access to systems or configurations is restricted.
- The root cause cannot be identified with available evidence.
- Engineering or infrastructure teams are required to implement the fix.

## Lessons Learned

Document the root cause, fix, and preventive recommendations.

## Key Concepts

### SPF
Defines which mail servers are authorized to send email for a domain.

### DKIM
Verifies that messages are digitally signed by authorized systems.

### DMARC
Defines how receiving servers should handle messages that fail authentication checks.
