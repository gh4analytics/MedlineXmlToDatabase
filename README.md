MedlineXmlToDatabase
====================

This is a Java application for loading MEDLINE XML files into a relational database (currently supporting SQL Server and PostgreSQL). The application was designed with two goals in mind:

1. Everything in the XML files needs to go into the database.

2. Any changes in the XML structure that occur over the years should not require changing the program.

The application is run in two phases:

1. During *analysis*, the structure and contents of a large set of XML files is analysed, and a database structure is build to accomodate the data. This is typically done only once a year.

2. During *parse*, all XML files in a folder are parsed and their contents are inserted into the database. This is typically done every time new XML files are available from MEDLINE.

This is still very much work in progress. See the MainClass to see how one could run this Java project.

Note that the application works directly of the GZipped XML files, so no need to unzip them.
