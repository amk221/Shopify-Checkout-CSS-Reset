# :department_store: Shopify-Checkout-CSS-Reset

### What does it do?

It 'turns off' Shopify's stylesheets during the 3 step checkout:process (including the mobile styles!)

* Step 1 being:
  Discounts, Shipping method and Newsletter
* Step 2 being:
  Order processing screen (spinner)
* Step 3 being: 
  The Thankyou page
    
### Why?
    
Shopify's checkout pages are notoriously tricky to style, especially if you are creating a responsive design.

Shopify **does not inlcude** the essential viewport meta tag unless `checkout.mobile.css.liquid` is present in your theme... and even if it is, they lump you with another set of styles to tweak and override.

This reset stylesheet allows you to create a single responsive stylesheet rather than two depending on the environment.

You may be able to get away with _not_ creating the mobile stylesheet (and therefore not using the viewport meta tag), but instead using the CSS [viewport declaration](//www.google.com/search?q=css+viewport+declaration). However at the time of writing it was not widely supported.

### How does it work?

This reset stylesheet was created by combining all the selectors & properties from Shopify's checkout stylesheet with those from their mobile checkout stylesheet. Then, each property's value was reset. Thereby maintaining the same specificity, hence it is a pretty brutal reset, which includes some !important rules. 



