# Feature 1


## Stories


### Scenario 1


```
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

                                    |   Business    |   FE-Prototype   | BE-Design  | FE-implement  | BE-implement
1.  Authentication and Focus        |               |                  |            |               |    
    1.1 Authenticated Page          |               |                  |            |               |
    1.2 Navigate to Voucher Store   |               |                  |            |               |
2.  Purchase Voucher                |               |                  |            |               |
    2.1 Choose                      |               |                  |            |               |
    2.1 Pay                         |               |                  |            |               |
3.  Apply Voucher                   |               |                  |            |               |
    3.1 Choose Item                 |               |                  |            |               |
    3.2 Apply voucher               |               |                  |            |               |
    3.3 Payment                     |               |                  |            |               |
