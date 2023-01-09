# Proposal

## Voucher Ecosystem

### Introduction

Consumer-oriented applications are widely used to provide goods and services via digital payments. Often, in-app vouchers are issued to encourage consumers to spend and increase order value. Today, foodpanda offers vouchers in the form of "promo code" or "voucher code" to be exchangeable for a voucher. These vouchers are generated in-house for foodpanda campaigns targeting specific product lines, locations and vendors (to name a few policy parameters). In the foodpanda app, a consumer exchanges these voucher codes for vouchers which are saved in their account.

```txt
    --- Current Flow ---
1.  foodpanda generates and advertise voucher codes.
2.  Consumer saves voucher via voucher code.
3.  Consumer applies the voucher during checkout.
```

## Problem Statement

### Hypothesis

We propose to introduce dollar-for-dollar gift vouchers that are transferrable and purchased by consumers with the assumed benefits:

1. Value Lock-in - Capture spending avenue from consumer and obtain early cash flow from voucher purchases.
2. Social Engagement - Increase user in-app activity and consumer-to-consumer interaction. We also hope this feature broadens user account base by providing a motivation to sign up with foodpanda. (customer acquisition)

### Preliminary Feature Flow

A high-level process is described below (exact mechanism will be further elaborated on prototype and system design):

```txt
    --- A user purchases, owns and applies a voucher

1.  Consumer logins.
2.  Consumer purchases a voucher.
    // payment applies // consumer owns the voucher on purchase.
3.  Consumer applies the voucher during checkout.
```

```txt
    --- A user purchases and owns a voucher. The voucher is transferred to a second user. The second user

1.  Consumer1 logins.
2.  Consumer1 purchases a voucher.
    // a voucher code is tied to the voucher
3.  Consumer1 shares voucher code to Consumer2
4.  Consumer2 logins.
5.  Consumer2 saves the voucher via voucher code.
    // Ownership transferred.
6.  Consumer applies voucher during checkout.
```
