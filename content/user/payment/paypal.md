---
title: PayPal
description: PayPal in Zen Cart
category: payment
weight: 10
---

#### Express Checkout

Follow this link for [Setup instructions for Express Checkout](/user/payment/paypal_express_checkout). 

#### Website Payments Standard

You REALLY SHOULD USE EXPRESS CHECKOUT!!!

In case it wasn't said already: You should NOT be using Payments Standard; you should be using Express Checkout which is far more reliable.

But, if you insist on using the older technology of Website Payments Standard, follow these instructions:

This applies to North American PayPal™ users (and maybe others too).

Important: If you're reading this far then you've ignored the important notices above: You should be using Express Checkout instead of Payments Standard. Seriously.

Now, re-read the sentence above.

And once again.

If you're truly choosing to ignore the important advice to use Express Checkout instead, the following settings are required to use Payments Standard:

**ON THE PAYPAL™ WEBSITE**

1.  Log in.
2.  Click on _Profile_.
3.  Click on _Email_.
4.  Write down your _primary_ email address. You need to use this exact email address in your Zen Cart™ settings in the next section below.
5.  Click on Profile again.
6.  Click on Instant Payment Notification Preferences.
7.  Click on Edit.
8.  Turn it on (check the box).
9.  Set the URL to: `https://www.YOURSTORE.com/ipn_main_handler.php`. (The complete correct URL can be obtained from your Admin area inside the PayPal payment module's information settings.)
10.  Click Save.
11.  Click on Profile.
12.  Click on My selling tools.
13.  Click on Website Payment Preferences.
14.  Auto Return for Website Payments - set to on.

Provide the Return URL (obtain correct URL from your Zen Cart admin ... it will take the form of something like the following examples): `https://www.YOURSTORE.com/index.php?main_page=checkout_process`

15.  Other settings in this area can be set based on your preferences. Consult PayPal™ for their meanings.

My selling tools -> Website Preferences -> Payment Data Transfer ... If you're using PDT, make sure you have the same token in Zen Cart as you have in PayPal.

Encrypted Website Payments ... set this to OFF. Zen Cart does not currently support this option.

PayPal™ Account Optional ... if you want to allow customers to pay by credit card and not have to create a PayPal™ account, set this to ON

16.  Click _Save_.
17.  If your website's language is not a Western/European language, go to Language Encoding and set your language.
18.  **Turn off ALL tax and shipping settings in your PayPal™ account**. These will cause your transaction amounts to not match Zen Cart™ amounts, and thus your orders will not be released.
19.  Oh ... and ... if you've never had your PayPal™ account "verified", you should follow their steps to do so.

**IN ZEN CART™**

1.  Go to Admin -> Modules -> Payment -> PayPal
2.  If this is the first time configuring for PayPal™ on this site, then you need to click on _Install_.
3.  Otherwise, click on _Edit_.
4.  Enter the primary email address of your PayPal™ account.
5.  Configure any other options as desired.
6.  Note the URL's suggested in the top of the PayPal™ module's instructions - they should match what you have set in your PayPal™ profile in the steps above for the PayPal™ site.

### Using PayPal on Multiple Sites

See this FAQ Article: [Using PayPal on Multiple Sites](/user/payment/paypal_multiple_sites). 

#### Express Checkout

You can use a single PayPal™ account to collect payments from multiple Zen Cart™ sites simply by following the "In Zen Cart™" instructions above, for each site. Zen Cart™ will send override information to PayPal™ to let them know which store to send its notifications to.

#### Website Payments Standard

You REALLY should be using Express Checkout instead.

But if your mind is really made up to use Payments Standard anyway, then if you use your PayPal™ account on non-Zen Cart™ sites or on eBay™ or perhaps on a WordPress site, **be sure that you have all "taxes" and "shipping" options disabled in your PayPal™ profile**; otherwise these charges will be added to your Zen Cart™ orders and cause them to not match, and therefore they won't be released or added to your orders list.

### Things to check if it's not working (Website Payments Standard specifically)

These are the common mistakes causing Website Payments Standard transactions to fail:

1.  Check that the email address you enter for PayPal™ in Zen Cart™ admin matches CaSE-SenSItiVE exactly with your PRIMARY email address setting in your PayPal™ account profile on PayPal's™ site.
2.  Is your PayPal™ account "verified" yet?
3.  Is your PayPal™ account a "Business" account? (Business is preferred. Premier can be used in some cases (Ask your PayPal rep if unsure). Personal cannot.)
4.  Check your PayPal™ profile settings on [paypal.com](http://paypal.com/)
    *   In **Website Payment Preferences**, your Return URL should be set to your site's checkout_process page. (ie: `http://www.YOURSITE.com/directory/index.php?main_page=checkout_process`).
    *   It is advisable to have Auto Return set to On.
5.  **Turn off ALL tax and shipping fees in your PayPal™ profile**. They will cause the purchase price to mismatch when returning to Zen Cart™.
6.  NOW, **also check the following list of IPN issues** as well _(see below)_

### Things to check if it's not working (IPN communications in general)

These are the common configuration errors causing IPN processing to fail:

1.  If it "was" working, but stopped, make sure PayPal's services are running properly. Check [PayPal Live Server Status](https://www.x.com/community/ppx/system_status).
2.  Make sure your site is *not* in down-for-maintenance mode.
3.  Make sure your site does *not* have password-protection via .htaccess in order to get to the "store" area.
4.  Check with your host that the server is able to do outbound TLS connections
5.  Use your browser and go to the Login page of your store. If the page is SSL, do you get any certificate errors in your browser? Test from a couple different computers that you don't normally use. An invalid SSL certificate or one that has errors of any sort, could prevent PayPal from successfully posting the notices to your site.
6.  Try accessing `http://YOURSITE.com/ipn_main_handler.php` with your browser. If you see PHP errors, those will need to be resolved. If you get a white screen, then the first phase of PayPal™ contacting your site isn't encountering errors. This doesn't mean there aren't any, it just means the initial most obvious steps are working.
7.  There are [two communication testing tools available in the support forum](https://www.zen-cart.com/forum/showthread.php?t=65680). If you are asking for troubleshooting help, please supply the URL to each of these tools after you have installed them on your site, so we can assess the responses they reveal.
8.  Turn on [debug logging](https://www.zen-cart.com/forum/showthread.php?t=61199) in your PayPal™ module, and post a link to the zipped log files so they can be analyzed. You'll need to check to be sure that your _/logs_ folder is marked read/write (chmod 777). Then use your [FTP tool](/user/first_steps/useful_tools/#ftp-tools) to access/view those logs and zip-and-upload them for analysis.
9.  Check there is no IP block or firewall to prevent PayPal's™ servers from talking to your server (your host should check this, and you should check any blocking you may have done via your control panel. Also check .htaccess for any _deny from_ statements and be sure none of them are addresses related to PayPal™.
    *   [PayPal IP Address List](https://ppmts.custhelp.com/cgi-bin/ppdts.cfg/php/enduser/std_adp.php?p_faqid=92) (these should be in your host's firewall whitelist)
    *   AND the IP addresses on PayPal's [Go Live Checklist](https://cms.paypal.com/us/cgi-bin/?cmd=_render-content&content_ID=developer/howto_api_golivechecklist) page
    *   For sandbox testing, also open: ipn.sandbox.paypal.com
10.  You may find it helps to Uninstall ("remove") and Re-Install the payment module in Zen Cart™ admin.
11.  When you use two PayPal™ accounts to make a simulation, make sure you're using the right account.
12.  Check your PayPal™ profile settings on [paypal.com](http://paypal.com/)

*   You need your **Instant Payment Notification preferences** ON

*   Instant Payment Notification URL must be set to a valid address. Normally this is the URL of your site's `ipn_main_handler.php` (ie: `http://www.YOURSITE.com/ipn_main_handler.php` or `http://www.YOURSITE.com/directory/ipn_main_handler.php` ) However, if you're running Website Payments Standard on another website, you can leave THAT site's URL there instead, as long as it's actually working properly.

13.  Using your hosting control panel, find the "Error Log" option, and check your server's errorlog entries to see if any attempts to access your site's `ipn_main_handler.php` file are being denied for any reason.
14.  If you have a SEFU or SEO contribution installed, try removing it and testing again. Some are not configured to allow PayPal processing.
15.  If you're using Payflow Pro (or Website Payments Pro UK), check your PayPal Manager area for any IP address restrictions. If you've got it restricted to only accept payment requests from certain IP addresses, make sure your webserver's IP address is in the list. Or clear the list out completely. A call to PayPal tech support can verify whether they have any additional IP addresses recorded that you can't see.
16.  You can check whether PayPal has tried to send you IPN notifications that have failed, and re-send them if needed. In your PayPal account, in the My Account tab, go to the History menu and choose the IPN History option. Tick the relevant boxes and press "Resend selected". If there are many "failed", it's best to start with just checking ONE and attempting Resend. Then check your store to see if it comes through (give it 10-30 minutes). If it doesn't show up in your store, check the IPN debug logs on your server and see what errors have been recorded there.

### How Does IPN work (for Website Payments Standard)?

"IPN" = "Instant Payment Notification" ... part of PayPal's™ "Website Payments Standard" service.

1.  Customer places an order on your site
2.  For payment, they are taken to a link on PayPal's™ site, where they provide their information and pay for their order.
3.  They click a link when finished (or wait 5 seconds) and return to your site.

Meanwhile, between steps 2 and 3 above, PayPal's™ server does this:

1.  PayPal's™ server sends a request to your website...which is waiting and listening for connections from PayPal™ to the `ipn_main_handler.php` page.
2.  Your server sits waiting and listening for hits to ipn_handler.php.
3.  When your server receives a request, it attempts to validate and be sure that the PayPal™ data provided matches the order details for which it is intended.
4.  If validation passes, the customer's order is released, and it lets the PayPal™ server know that you received their confirmation. This handshaking happens via CURL on port 443, and requires that your server be configured for modern TLS communication to https URLs.
5.  **NOTE:** PayPal's™ server will attempt the IPN notification (hourly) for up to four days if it's not successful on the first try. In this case your customer's order will not show up in your Admin until the IPN notification is successful.

## Testing PayPal™ Transactions

To test that PayPal™ is properly configured, you should test two methods:

1.  Test by paying for something using a PayPal™ account (not the same account as your store).
2.  Test by paying for something with a credit card WITHOUT creating or using a PayPal™ account for payment.

All of these tests are to be performed in "production" or "live" mode. Do NOT use a Sandbox for testing. _(If you don't know what this means, just proceed with testing.)_

### Testing using a PayPal™ account

1.  You need a second PayPal™ account to do this. PayPal™ allows you to have two accounts per person: one personal and one business. For this test, you will pay for your purchase using funds on account in your personal PayPal™ account. You will be paying money to your store account (and refunding it).
2.  Create or select a product which has a low price, such as $0.01 or maybe $1.00.
3.  Purchase that product.
4.  During checkout, choose the lowest-price shipping option.
5.  During checkout, choose PayPal™.
6.  After the Checkout Confirmation screen, you'll be taken to the PayPal™ website to make payment.
7.  Enter your PERSONAL PayPal™ account username and password.
8.  Confirm the transaction.
9.  You will be returned to your store after completion.
10.  Verify that you received two or three emails: one from PayPal™, one from the store to you as a customer, and one from the store to your _Admin_ address. If you did not receive the emails from the store within five minutes, then go to the Troubleshooting section of this document, above.
11.  Log in to your BUSINESS PayPal™ account and refund your test transaction.

### Testing without a PayPal™ account

To test payment by credit card without using a PayPal™ account, use these steps:

_(Before proceeding, find your credit cards, and select one that's not already associated with any PayPal™ account !!)_

1.  Create or select a product in your store which has a low price, such as $0.01 or maybe $1.00.
2.  Purchase that product.
3.  During checkout, choose the lowest-price shipping option.
4.  During checkout, choose PayPal™.
5.  After the Checkout Confirmation screen, you'll be taken to the PayPal™ website to make payment.
6.  Underneath the login box for PayPal™ username/password, there is a link to Purchase without a PayPal™ account. Click that link.
7.  Fill in and/or confirm your personal information.
8.  Fill in your payment details including credit card number. (You should NOT use a credit card number that's already associated with any PayPal™ account !!)
9.  Confirm the transaction.
10.  You will be returned to your store after completion.
11.  Verify that you received two or three emails: one from PayPal™, one from the store to you as a customer, and one from the store to your _Admin_ address. If you did not receive the emails from the store within five minutes, then go to the Troubleshooting section of this document, above.
12.  Log in to your BUSINESS PayPal™ account and refund your test transaction.

