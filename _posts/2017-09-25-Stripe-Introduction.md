---
layout: post
title: Stripe Is Fun
date: 2017-09-25 13:32:20 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: stripe.png # Add image post (optional)
tags: [Stripe, Samsung, NewTech]
---

# Stripe Is Fun

## Quick Start
### Basic Operations
#### Key Concepts in Stripe:
*   Card: A simple card. Represent by a token. Can use this token to make an one time payment but not recurring payment.
*   Customer: Centre concept in stripe. A recurring payment can only happen in the user level.
*   Plan: A plan is a special setting for a recurring payment. You can add this plan to any customer.
*   Subscription: We can add a customer to subscript a plan.

#### Stripe 101
1.  Create a card with Stripe.js elements so key info such as card number, cvv, or expire number won't go through our server.  

```javascript
var stripe = Stripe('publishable key');
var elements = stripe.elements();

var card = elements.create('card');
card.mount('#card-element');

var promise = stripe.createToken(card);
promise.then(function(result) {
  // result.token is the card token.
  token = result.token;
});
```

3.  After we get the token, we can make a one time payment directly in the server side with our secret key. Always keep the secret key inside server side. Publish it can make a disaster.  

```go

```
