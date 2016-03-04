---
layout: post
title: Create your own Androidpay tokens
---
Androidpay is Google's answer to Apple's attempt to dominate the mobile payment market with its Applepay brand. A market which is wide open in America with its massive meltdown of credit card security, with breach after breach of payment systems.
The Credit Card companies are now scrambling to replace the ancient magnetic stripe cards  which are costing them [billions](http://www.creditcards.com/credit-card-news/credit-card-security-id-theft-fraud-statistics-1276.php) yearly in fraud. There are many possible technologies ready to replace them, [EMV](https://www.emvco.com/) being the most widely used.

### Two ways to pay

Both Applepay and Androidpay do the same thing, they wrap the credit card data with an extra layer of security. With both Applepay and Androidpay you can pay in two different ways.
Either at a payment (POS) terminal in physical store or online with an App or website on your mobile phone.
If you pay at a POS terminal you are basically using [EMV-NFC](http://www.smartcardalliance.org/publications-emv-and-nfc-complementary-technologies-enabling-secure-contactless-payments/). In that case there is very little difference between Applepay or Androidpay and a normal NFC-enabled EMV Credit Card. Your phone is talking the EMV protocol with the POS terminal.

### Androidpay Tokens

When paying with an App or website on your phone your Credit Card details are encrypted in a unique way that Google designed. This encrypted Card is called a payment token.
Google provides excellent [documentation](https://developers.google.com/android-pay/integration/gateway-processor-integration) on how to decrypt their payment tokes.
When you need to create your own test tokens or recrypt existing tokens you can use their example decryption code. All you need to do is invert the encryption steps.
