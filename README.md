Getting started with Odoo
-------------------------------
Installing odoo11 - Windows x64 
-------------------------------
Prerequisite
git for Windows 2.13.2 or + 
https://git-scm.com/downloads

nodejs 6.10 + 
https://nodejs.org/en/download/

python 3.5.4
https://www.python.org/downloads/windows/

psycopg2 2.6.2 - driver
http://initd.org/psycopg/download/

wkhtmltopdf 0.12.4 +
https://wkhtmltopdf.org/downloads.html

postgresql 9.6.6 or +
https://www.postgresql.org/download/

odoo11 or +
https://github.com/odoo/odoo

1.0 Installation
1.1 install git for Windows and add to PATH. (i.e so you can call from the CLI)
1.2 install nodejs and add to PATH.
1.3 install python3 and add to PATH. (for same reason in step 1)
1.4 install psycopg2, make sure it has detect python3 in the installation diectory. (if it didn't then check your python installation)
1.4.1 install postgresql set password, leave the default port of 5432 (if you change it, na your wahala), leave the default locale. 
1.4.2 add C:\Program Files\PostgreSQL\9.6\bin to PATH.

2.0 downloading odoo11
2.1.0 now clone odoo11 source from github
2.1.1 open cmd (change directory to a location you want to keep odoo11 prefered C:\)
2.1.2 type git clone https://github.com/odoo/odoo.git

3.0 configuring postgreSQL
3.1 open pgAdmin4, under servers, click the dropdown and enter pass (the password you typed during installation refer 1.4.1)
3.2 under Login/Group Roles (2), right click -> create -> Login/Group Role..
3.2.1 enter name 'odoo' under the general tab, password 'odoo' under definition tab and grant all privileges to user 'odoo' under the privileges tab and save.

4.0 configuring and installing odoo11
4.1 open cmd and change directory to odoo (refer to 2.1.1)
4.1.1 now copy the directory path of pip to cmd and run install -r requirements.txt (dir of pip: C:\Users\'username'\AppData\Local\Programs\Python\Python35\Scripts\pip.exe)
4.1.1.1 like this C:\Users\'username'\AppData\Local\Programs\Python\Python35\Scripts\pip.exe install -r requirements.txt
remember doing this will install all the python libraries required to run odoo, go take coffee break as it downloads.
4.2 run npm install -g less
4.3 congratulations... your odoo installation is now complete.

5.0 running odoo
5.1 run odoo by typing python odoo-bin -w odoo -r odoo
