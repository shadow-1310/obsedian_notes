## manuals
- [How to Disable Secure\_file\_priv option in MySQL - Linux - Techglimpse](https://techglimpse.com/secure_file_priv-mysql-option/)
- [MySQL :: MySQL 8.0 Reference Manual :: 3.3.3 Loading Data into a Table](https://dev.mysql.com/doc/refman/8.0/en/loading-tables.html)
- [MySQL :: MySQL 8.0 Reference Manual :: 13.2.9 LOAD DATA Statement](https://dev.mysql.com/doc/refman/8.0/en/load-data.html)
## errors
### error code: 3948  and then 2098- loading local data is disabled
- References
	- [mysql - ERROR: Loading local data is disabled - this must be enabled on both the client and server sides - Stack Overflow](https://stackoverflow.com/questions/59993844/error-loading-local-data-is-disabled-this-must-be-enabled-on-both-the-client)
		- ![[Pasted image 20230811020848.png]]
	- this is another similar approach from the same stackexchange page
		- ![[Pasted image 20230811021004.png]]
	- [enabling local infile in server](https://stackoverflow.com/questions/66848547/mysql-error-code-3948-loading-local-data-is-disabled-this-must-be-enabled-on-b)
	- [MySQL Workbench8: Enable LOAD DATA LOCAL INFILE(with error code : 3948) - Stack Overflow](https://stackoverflow.com/questions/61749842/mysql-workbench8-enable-load-data-local-infilewith-error-code-3948)
- Procedure
	- connect to sql server from terminal
		 ```sh
		sudo mysql
	     ```
	 - Now type the following command
		```sh
		SHOW GLOBAL VARIABLES LIKE 'local_infile';
		```
		- it will display the following table but Value will be **OFF**
			- ![[Pasted image 20230811015505.png]]
		- Now give the following command to make it **ON** like above
			```sh
			SET GLOBAL local_infile = true;
			```
	- Now we have to edit /

### import while having mismatched columns
- [csv - MySQL - Multiple set on LOAD DATA INFILE - Stack Overflow](https://stackoverflow.com/questions/12530971/mysql-multiple-set-on-load-data-infile)
- [CSV Load Data into mySQL with mismatched and skipped columns - Stack Overflow](https://stackoverflow.com/questions/53464816/csv-load-data-into-mysql-with-mismatched-and-skipped-columns)

### column values have 'comma'(,) in them and some enclosed by ""
- [csv - MySQL "LOAD DATA INFILE" and Missing Double Quotes - Stack Overflow](https://stackoverflow.com/questions/5904909/mysql-load-data-infile-and-missing-double-quotes)