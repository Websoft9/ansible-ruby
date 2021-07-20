# Initial Installation

If you have completed the Ruby Runtime deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check you **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the TCP:80 is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for Ruby Runtime

## Usability test

1. Using local Chrome or Firefox to visit the URL *http://DNS* or *http://Instance's Internet IP*, access Rails example page
   ![Ruby Rails](https://libs.websoft9.com/Websoft9/DocsPicture/en/ruby/ruby-railsgui-websoft9.png)

2. Using local Chrome or Firefox to visit the URL *http://Internet IP/9panel* to enter the boot page
   ![9panel](https://libs.websoft9.com/Websoft9/DocsPicture/en/9panel/9panel-ruby-websoft9.png)

3. You can get the basics of image, manage the database, access docs, and helpdesk from 9Panel

## Log in Database

Ruby Runtime includes MySQL and Web-GUI tool `phpMyAdmin`, [Log in MySQL](/zh/admin-mysql.md) to manage your database now

![9panel](https://libs.websoft9.com/Websoft9/DocsPicture/en/9panel/9panel-mysql-websoft9.png)

## Application Installation

You can install multiple applications on Ruby Runtime, refer to [Applications Deployment](/solution-addapps.md)

## Q&A

#### I can't visit the start page of Ruby Runtime?

Your TCP:80 of Security Group Rules is not allowed so there no response from Chrome or Firefox

#### What's 9Panel?

[9Panel](https://github.com/Websoft9/9panel) is an opensource component included in some image of Websoft9, it is powered by Websoft9. 9Panel is a set of HTML pages for quickly using image of Websoft9. You should delete all the files in 9Panel folder if you do not want to delete 9Panel