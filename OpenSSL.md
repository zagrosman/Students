Steps to download, compile, and install are as follows (I'm installing version 1.0.1g below; please replace "1.0.1g" with your version number):

Step – 1 : Downloading OpenSSL:

Run the command as below :

$ wget http://www.openssl.org/source/openssl-1.0.1g.tar.gz

Also, download the MD5 hash to verify the integrity of the downloaded file for just varifacation purpose. In the same folder where you have downloaded the OpenSSL file from the website :

$ wget http://www.openssl.org/source/openssl-1.0.1g.tar.gz.md5
$ md5sum openssl-1.0.1g.tar.gz
$ cat openssl-1.0.1g.tar.gz.md5

Step – 2 : Extract files from the downloaded package:

$ tar -xvzf openssl-1.0.1g.tar.gz

Now, enter the directory where the package is extracted like here is openssl-1.0.1g

$ cd openssl-1.0.1g

Step – 3 : Configuration OpenSSL

Run below command with optional condition to set prefix and directory where you want to copy files and folder.

$ ./config --prefix=/usr/local/openssl --openssldir=/usr/local/openssl

You can replace “/usr/local/openssl” with the directory path where you want to copy the files and folders. But make sure while doing this steps check for any error message on terminal.

Step – 4 : Compiling OpenSSL

To compile openssl you will need to run 2 command : make, make install as below :

$ make

Note: check for any error message for verification purpose.

Step -5 : Installing OpenSSL:

$ sudo make install

Or without sudo,

$ make install

That’s it. OpenSSL has been successfully installed. You can run the version command to see if it worked or not as below :

$ /usr/local/openssl/bin/openssl version

OpenSSL 1.0.1g 7 Apr 2014
