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

Confirm successful delivery after DNS propagation and testing.

## Lessons Learned

Document the root cause, fix, and preventive recommendations.
