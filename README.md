# adelia9

Do not use adelia9 - use https://github.com/tinyib/tinyib/  instead because it is the original staring point. Also the codebase in adelia9 is going to be drastically changed. 


A fork of tinyib made for php 8.1.x  - With plans to drastically slim it down and re-work some of the code. The reason for the slimming is to focus on one
db mode, that way it is easier to maintain. Also there are a couple minor problems with php 8.2 beta so minor purges of code and slight re-writes from scratch will have
to happen. That is for php 8.2, but for now everything works with php 8.1.x 

PRO TIP- If you try to get current latest tinyib working on php 8.1.X and it gives an error message similar to:
"implicit conversion from float 8.65 to int loses precision in functions.php line 780" - it has to do with a deprication
of a math function. (PHP 8.1: Implicit incompatible float to int conversion is deprecated) -- Converting a float number to an integer 
often involves losing the fractional value of the float number. For example, 6.8, a float number, will be 6 when converted to an integer. 
In dynamically typed programming languages such as PHP, sometimes this conversion is unintended and undesirable. PHP is steadily improving the
rules of its dynamic type coercing rules to be more predictable and intuitive. PHP 8.0 has improvements such as locale-independent float to string
conversion and numeric string comparison improvements. From PHP 8.1, a deprecation notice is emitted when a float value is coerced to an int value
implicitly, and lost the fractional value in the process. This deprecation notice is not emitted when a float value is explicitly converted to an integer.
The behavior of Strict Types has not changed. When Strict Typing is enabled, PHP continues to throw a TypeError exception on every implicit type coercion. 
Further, explicitly casting to integers ((int) $floatNum) or and the floatval functions are not affected. <<<< TO SOLVE this entire deprication on php 8.1.x
all you have to do is change the photo sizes to an odd number. For example, define('TINYIB_MAXWOP', 250);   define('TINYIB_MAXHOP', 250);  define('TINYIB_MAXW', 250);          
define('TINYIB_MAXH', 250); resolves to a float 8.65 to int. Change the 250 to 251 in all four places, then the math makes a number without a floating integer, 
(a decimal point) and the deprication error never shows or is an issue. ALSO, strftime is depricated, and the php manual says to go with date() instead. 
OF NOTE, pho 8.2 throws a couple new errors, and the simple captcha no longer functions and the youtube embed no longer functions. It will probably be easiest to purge 
the old code entirely for both and hand code a new simple captcha and YT embed. 

Adelia 9 will be obsolete when php 8.2 comes out soon. Tinyib in any form is never obsolete, it serves as the base for an imageboard to work in any php version. Tinyib
has always had that utility - it has always has that unique merit. 



