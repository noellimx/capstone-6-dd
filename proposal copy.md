Proposal

# Voucher Ecosystem


## Glossary and Terms

## Problem Statement

### Introduction

Consumer-oriented applications are widely used to provide goods and services via digital payments. Often, in-app vouchers are issued to encourage consumers to spend and increase order value. Today, foodpanda offers vouchers in the form of "promo code" or "voucher code" to be exchangeable for a voucher. These vouchers are generated in-house for foodpanda campaigns targeting specific product lines, locations and vendors (to name a few policy parameters). In the foodpanda app, a consumer exchanges these voucher codes for vouchers which are saved in their account.

```
1.  foodpanda_campaign::generate_vouchers(product_line, location, vendor, quantity, type, ...) -> (voucher_codes)
    // vouchers are advertised/marketed, then
2.  consumer::save(voucher_code) -> saved_voucher
3.  consumer::pay(product_line, items, saved_voucher, [destination], [time], ...) -> ok
```

### Hypothesis

We propose to introduce dollar-for-dollar gift vouchers that are purchased by consumers and transferrable with the assumed benefits:

1. Value Lock-in - Capture spending avenue from consumer and obtain early cash flow from voucher purchases.
2. Social Engagement - Increase user in-app activity and consumer-to-consumer interaction. We also hope this feature broadens user account base by providing a motivation to sign up with foodpanda.


### Preliminary Feature Flow

A high-level process is described below (exact mechanism will be further elaborated on prototype and system design):

```
    --- A user purchases, owns and applies a voucher
1.  login(credentials) -> consumer
2.  consumer::voucher::purchase(value) -> saved_voucher

3.  consumer::pay(product_line, items, saved_voucher, [destination], [time], ...) -> ok
```


```
    --- A user purchases and owns a voucher. The voucher is transferred to a second user. The second user 
1.  login(credentials1) -> consumer1
2.  consumer1::voucher::purchase(value) -> saved_voucher
    // consumer1 provides saved_voucher.transfer_code to consumer 2
3.  login(credentials2) -> consumer2
4.  consumer2::voucher::save(saved_voucher.transfer_code) -> saved_voucher
    // saved_voucher will be owned by consumer2 instead of consumer1
5.  consumer2::pay(product_line, items, saved_voucher, [destination], [time], ...) -> ok

