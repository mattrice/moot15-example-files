# moot15-example-files
US Moodle Moot 2015

# Reaching a particular server based on a browser cookie

This is a very useful technique for debugging/testing: you can set debugging on in config.php on a single server that only you can access, and then you can enjoy the full benefits of debug output/logging without affecting anyone else using your Moodle.

I have included the file manage_lb_cookies.php to allow easy access to setting/clearing the appropriate cookie.

What happens if your cookie asks for a server that is not available? Your traffic will be load-balanced as if you did not have the cookie set.