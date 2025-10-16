# Implementing Cloud SQL

# **Overview**

In this lab, you configure a Cloud SQL server and learn how to connect an application to it via a proxy over an external connection. You also configure a connection over a Private IP link that offers performance and security benefits. The app we chose to demonstrate in this lab is Wordpress, but the information and best practices are applicable to any application that needs SQL Server.

By the end of this lab, you will have 2 working instances of the Wordpress frontend connected over 2 different connection types to their SQL instance backend, as shown in this diagram:

[SQL Lab Diagram](https://cdn.qwiklabs.com/QF444W9Ieg9pVOpgBxvJlyFcbpc5Mc9%2BAtM1A1T3gBA%3D)

# **Objectives**

In this lab, you learn how to perform the following tasks:

- Create a Cloud SQL database
- Configure a virtual machine to run a proxy
- Create a connection between an application and Cloud SQL
- Connect an application to Cloud SQL using Private IP address