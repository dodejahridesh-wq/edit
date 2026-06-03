---
name: stripe-payment
description: >
  Online payment API infrastructure and integrations.
---

# Stripe Payment API

## Overview
Stripe provides a robust set of REST APIs that allow businesses to accept payments, manage subscriptions, run billing logic, and track payouts online.

## Python Integration
```python
import stripe
stripe.api_key = "sk_test_..."

# Create a PaymentIntent
intent = stripe.PaymentIntent.create(
  amount=2000, # $20.00
  currency="usd",
  payment_method_types=["card"],
)
print(intent.client_secret)
```

## CLI Commands
```bash
# Trigger a webhook event for local testing
stripe trigger payment_intent.succeeded

# Forward webhooks to local server
stripe listen --forward-to localhost:3000/webhooks
```
