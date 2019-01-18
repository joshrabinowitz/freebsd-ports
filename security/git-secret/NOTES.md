# Notes for freebsd ports package of git-secret

## See FreeBSD Porters Handbook <https://www.freebsd.org/doc/en_US.ISO8859-1/books/porters-handbook/porting-desc.html>

## From section 3.4 Testing the Port, Recommended Test Ordering

-   make stage			(OK)
-   make check-orphans		(OK)
-   make package		(OK)
-   make install		(OK)
-   make deinstall		(OK)
-   make package (as user)	(NOT TESTED, expected to work)

