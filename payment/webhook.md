# Webhook

## Purpose

Allow the payment gateway to notify the system about payment status changes.

## Why Webhook is Needed

Without a webhook:

- Customer may complete payment
- Browser may be closed
- System may not receive payment result

## Flow

Customer
→ Payment Gateway
→ Bank
→ Payment Gateway
→ Webhook
→ Backend System

## Business Rules

- Payment status must be updated based on webhook events.
- Duplicate webhook events must be ignored.
- Failed webhook processing should be retried.
