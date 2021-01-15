
Pagila
======

Pagila is a port of the Sakila example database available for MySQL, which was  
originally developed by Mike Hillyer of the MySQL AB documentation team. It  
is intended to provide a standard schema that can be used for examples in 
books, tutorials, articles, samples, etc.

Pagila works against PostgreSQL 11 and above.

All the tables, data, views, and functions have been ported; some of the
changes made were:

* Changed char(1) true/false fields to true boolean fields
* The last_update columns were set with triggers to update them
* Added foreign keys
* Removed 'DEFAULT 0' on foreign keys since it's pointless with real FK's
* Used PostgreSQL built-in fulltext searching for fulltext index.
  Removed the need for the film_text table.
* The rewards_report function was ported to a simple SRF

The schema and data for the Sakila database were made available under the BSD
license which can be found at http://www.opensource.org/licenses/bsd-license.php.
The pagila database is made available under this license as well.  


DUMP in csv format
---------------

This is a dump in CSV that can be used on AWS Glue and AWS Athena.


