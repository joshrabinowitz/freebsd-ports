# Notes for freebsd ports package of git-secret

## See FreeBSD Porters Handbook <https://www.freebsd.org/doc/en_US.ISO8859-1/books/porters-handbook/porting-desc.html>

## From section 3.4 Testing the Port, Recommended Test Ordering

-   make stage
-   make check-orphans
-   make package
-   make install
-   make deinstall
-   make package (as user)

