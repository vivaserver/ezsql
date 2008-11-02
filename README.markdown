PostgreSQL implementation of ezSQL 1.26 class forked to support PHP5
====================================================================

This little project started when I upgraded the server hosting a very important PHP4 application of mine to Apache2 and PHP5, resulting in the complete breakage of the database abtraction class being used: ezSQL version 1.26. The problem was that the PosgreSQL implementation of the ezSQL 1.26 class was incompatible with the new object model of PHP5.

ezSQL 2.04, the latest version as of this writing, already includes support for PostgreSQL (although earlier revisions of this new v2.0 didn't) so you'll probably be better off upgrading to it's most recent version anyway.

However, if you use PostgreSQL and need a quick drop-in replacement of ezSQL 1.26 to work with PHP5 this little fork might come useful.

This fork has been successfully tested on Ubuntu 6.06 with it's default package of PHP 5.1.2 and on Ubuntu 8.04 with PHP 5.2.4. Both running PostgreSQL 8.1.x. Please acknowledge success with other versions/distributions.


Usage
-----

    require "class.ez_sql.php";
    $db = new db("user","password","database","host"); 

Have fun,

Cristian R. Arroyo  
cristian.arroyo@vivaserver.com.ar