---
title: Detailed mysql index principle
date: 2022-08-11T07:32:19.731Z
summary: An index is a data structure that stores and sorts the values of one or
  more columns in a database table. It speeds up the search by reducing the
  number of records that need to be queried in a table. If there is no index,
  the database will have to perform Full table scan. The index is equivalent to
  the table of contents in the book, you can quickly find the content you need
  according to the page number on the table of contents, and improve the query
  speed.
draft: false
featured: false
authors:
  - ricear
tags:
  - INDEX
  - MYSQL
categories:
  - MYSQL
image:
  filename: featured.png
  focal_point: Smart
  preview_only: false
links:
  - name: Read More
    url: 'https://notebook.ricear.com/project-37/doc-720'
---
An index is a data structure that stores and sorts the values of one or more columns in a database table. It speeds up the search by reducing the number of records that need to be queried in a table. If there is no index, the database will have to perform Full table scan. The index is equivalent to the table of contents in the book, you can quickly find the content you need according to the page number on the table of contents, and improve the query speed.

By creating a unique index, the uniqueness of each row of data in the database table can be guaranteed. It can greatly speed up the data retrieval speed, avoid the data scanning of the whole table, and greatly reduce the number of matching rows traversed. This is also the main reason for creating an index. Can speed up the connection between the table and the table, especially in the realization of the referential integrity of the data is particularly meaningful. When using grouping and sorting clauses for data retrieval, the time for grouping and sorting in the query can be significantly reduced. By using the index, you can use the optimization hider in the query process to improve the performance of the system.

Click [here](https://notebook.ricear.com/project-37/doc-720) to see more information about the post.