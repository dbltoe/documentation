---
title: Configuration-My Store
category: admin_pages
weight: 10 
---

<h2 id="store_name">Store Name</h2>

<div class='indent'>The name of my store</div>


<h2 id="store_owner">Store Owner</h2>

<div class='indent'>The name of my store owner</div>


<h2 id="telephone__customer_service">Telephone - Customer Service</h2>

<div class='indent'>Enter a telephone number for customers to reach your Customer Service department. This number may be sent as part of payment transaction details.</div>


<h2 id="country">Country</h2>

<div class='indent'>The country my store is located in <br /><br /><strong>Note: Please remember to update the store zone.</strong></div>


<h2 id="zone">Zone</h2>

<div class='indent'>The zone my store is located in</div>


<h2 id="store_address_and_phone">Store Address and Phone</h2>

<div class='indent'>This is the Store Name, Address and Phone used on printable documents and displayed online</div>


<h2 id="expected_sort_order">Expected Sort Order</h2>

<div class='indent'>This is the sort order used in the expected products box.</div>


<h2 id="expected_sort_field">Expected Sort Field</h2>

<div class='indent'>The column to sort by in the expected products box.</div>


<h2 id="switch_to_default_language_currency">Switch To Default Language Currency</h2>

<div class='indent'>Automatically switch to the language's currency when it is changed</div>


<h2 id="language_selector">Language Selector</h2>

<div class='indent'>Should the default language be based on the Store preferences, or the customer's browser settings?<br /><br />Default: Store's default settings</div>


<h2 id="display_cart_after_adding_product">Display Cart After Adding Product</h2>

<div class='indent'>Display the shopping cart after adding a product (or return back to their origin)</div>


<h2 id="default_search_operator">Default Search Operator</h2>

<div class='indent'>Default search operators</div>


<h2 id="show_category_counts">Show Category Counts</h2>

<div class='indent'>Count recursively how many products are in each category</div>


<h2 id="show_category_counts__admin">Show Category Counts - Admin</h2>

<div class='indent'>Show Category Counts in Admin?</div>


<h2 id="show_linked_status_for_categories">Show linked status for categories</h2>

<div class='indent'>Show Category products linked status?</div>


<h2 id="tax_decimal_places">Tax Decimal Places</h2>

<div class='indent'>Pad the tax value this amount of decimal places</div>


<h2 id="display_prices_with_tax">Display Prices with Tax</h2>

<div class='indent'>Display prices with tax included (true) or add the tax at the end (false)</div>


<h2 id="display_prices_with_tax_in_admin">Display Prices with Tax in Admin</h2>

<div class='indent'>Display prices with tax included (true) or add the tax at the end (false) in Admin(Invoices)</div>


<h2 id="basis_of_product_tax">Basis of Product Tax</h2>

<div class='indent'>On what basis is Product Tax calculated. Options are<br />Shipping - Based on customers Shipping Address<br />Billing Based on customers Billing address<br />Store - Based on Store address if Billing/Shipping Zone equals Store zone</div>


<h2 id="basis_of_shipping_tax">Basis of Shipping Tax</h2>

<div class='indent'>On what basis is Shipping Tax calculated. Options are<br />Shipping - Based on customers Shipping Address<br />Billing Based on customers Billing address<br />Store - Based on Store address if Billing/Shipping Zone equals Store zone - Can be overridden by correctly written Shipping Module</div>


<h2 id="sales_tax_display_status">Sales Tax Display Status</h2>

<div class='indent'>Always show Sales Tax even when amount is $0.00?<br />0= Off<br />1= On</div>


<h2 id="show_split_tax_lines">Show Split Tax Lines</h2>

<div class='indent'>If multiple tax rates apply, show each rate as a separate line at checkout</div>


<h2 id="store_status">Store Status</h2>

<div class='indent'>What is your Store Status<br />0= Normal Store<br />1= Showcase no prices<br />2= Showcase with prices</div>


<h2 id="padss_admin_session_timeout_enforced">PA-DSS Admin Session Timeout Enforced?</h2>

<div class='indent'>PA-DSS Compliance requires that any Admin login sessions expire after 15 minutes of inactivity. <strong>Disabling this makes your site NON-COMPLIANT with PA-DSS rules, thus invalidating any certification.</strong></div>


<h2 id="padss_strong_password_rules_enforced">PA-DSS Strong Password Rules Enforced?</h2>

<div class='indent'>PA-DSS Compliance requires that admin passwords must be changed after 90 days and cannot re-use the last 4 passwords. <strong>Disabling this makes your site NON-COMPLIANT with PA-DSS rules, thus invalidating any certification.</strong></div>


<h2 id="padss_ajax_checkout">PA-DSS Ajax Checkout?</h2>

<div class='indent'>PA-DSS Compliance requires that for some inbuilt payment methods, that we use ajax to draw the checkout confirmation screen. While this will only happen if one of those payment methods is actually present, some people may want the traditional checkout flow <strong>Disabling this makes your site NON-COMPLIANT with PA-DSS rules, thus invalidating any certification.</strong></div>


<h2 id="admin_session_time_out_in_seconds">Admin Session Time Out in Seconds</h2>

<div class='indent'>Enter the time in seconds.<br />Max allowed is 900 for PCI Compliance Reasons.<br /> Default=900<br />Example: 900= 15 min <br /><br />Note: Too few seconds can result in timeout issues when adding/editing products</div>


<h2 id="admin_set_max_execution_time_for_processes">Admin Set max_execution_time for processes</h2>

<div class='indent'>Enter the time in seconds for how long the max_execution_time of processes should be. Default=60<br />Example: 60= 1 minute<br /><br />Note: Changing the time limit is only needed if you are having problems with the execution time of a process</div>


<h2 id="show_if_version_update_available">Show if version update available</h2>

<div class='indent'>Automatically check to see if a new version of Zen Cart is available. Enabling this can sometimes slow down the loading of Admin pages. (Displayed on main Index page after login, and Server Info page.)</div>


<h2 id="server_uptime">Server Uptime</h2>

<div class='indent'>Displaying Server uptime can cause entries in error logs on some servers. (true = Display, false = don't display)</div>


<h2 id="missing_page_check">Missing Page Check</h2>

<div class='indent'>Zen Cart can check for missing pages in the URL and redirect to Index page. For debugging you may want to turn this off. <br /><br /><strong>Default=On</strong><br />On = Send missing pages to 'index'<br />Off = Don't check for missing pages<br />Page Not Found = display the Page-Not-Found page</div>


<h2 id="currency_conversion_ratio">Currency Conversion Ratio</h2>

<div class='indent'>When auto-updating currencies, what "uplift" ratio should be used to calculate the exchange rate used by your store?<br />ie: the bank rate is obtained from the currency-exchange servers; how much extra do you want to charge in order to make up the difference between the bank rate and the consumer rate?<br /><br /><strong>Default: 1.05 </strong><br />This will cause the published bank rate to be multiplied by 1.05 to set the currency rates in your store.</div>


<h2 id="currency_exchange_rate_primary_source">Currency Exchange Rate: Primary Source</h2>

<div class='indent'>Where to request external currency updates from (Primary source)<br><br>Additional sources can be installed via plugins.</div>


<h2 id="currency_exchange_rate_secondary_source">Currency Exchange Rate: Secondary Source</h2>

<div class='indent'>Where to request external currency updates from (Secondary source)<br><br>Additional sources can be installed via plugins.</div>


<h2 id="html_editor">HTML Editor</h2>

<div class='indent'>Please select the HTML/Rich-Text editor you wish to use for composing Admin-related emails, newsletters, and product descriptions</div>


