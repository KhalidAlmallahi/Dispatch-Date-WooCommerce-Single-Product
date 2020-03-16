# WooCommerce: Display Dispatch / Estimated Delivery Date @ Single Product Page


A good way to inform online customers and avoid issues is showing the estimated delivery / dispatch time on the single product page, just below the “Add to Cart” button. Yes, you could do that manually by adding shipping info to each product short description, but the goal of Business Bloomer is to learn how to code that instead, so you won’t need to write things manually.

Also, this is great because if you change something in your dispatch rules, you just need to change the short PHP snippet and not all your product descriptions. It’s much more flexible this way.

Finally, in this post we’ll learn how to work with cut-off times (hour of the day) and current day of the week (pure PHP), so that we can show a “dynamic” notice based on current date. So, let’s see how it’s done!

<img src="https://businessbloomer.com/wp-content/uploads/2020/03/woocommerce-dispatch-orderby-shipping-estimate-date-1024x501.png">

# PHP Snippet: Display Dispatch / Estimated Delivery Date @ Single Product Page
Case scenario:

Friday/Saturday/Sunday orders ship on Monday
For other days, if before 4PM ships today…
…if after 4PM ships tomorrow
Please note the “date(‘N’)” and the “date(‘H’)” functions, which in PHP they respectively give me the current day of the week and current hour of the day so I can compare them with local & current time. Also look into “date_default_timezone_set()” function in case you want to set a different timezone, which is vital for this snippet’s calculations.

# Note:
This code add into function.php in your theme folder.

