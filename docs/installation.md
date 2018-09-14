How to install the blz language for various operating systems

## Already Installed?

You can update blz by running `blz-update`

## Windows

1.) Install the Java [JRE](http://www.oracle.com/technetwork/java/javase/downloads)

2.) Add the Java bin folder to your PATH ([help from oracle](https://www.java.com/en/download/help/path.xml))

3.) Download the [blz-ospl project from github](https://github.com/blazingkin/blz-ospl/archive/master.zip)

4.) Add the bin folder to your PATH

5.) From the command line, run

`blz -h`

## GNU/Linux

**Option 1 (installation script)**

Use the installation script [here](https://blazingk.in/install_blz_unix.sh)

or by

`curl https://blazingk.in/install_blz_unix.sh | bash` (Always read scripts you download before running them).

**Option 2 (manual)**

1.) Install Java

2.) Clone the blz-ospl project from github

3.) Add the blz-ospl 'bin' folder to your path

`echo 'export PATH=$PATH:INSTALLDIRECTORY/bin' >> ~/.bash_rc`

Where INSTALLDIRECTORY is the directory where you saved blz-ospl

4.) Reload your bash profile

`. ~/.bash_rc`

5.) From the terminal, run

`blz -h`

## MacOS

**Option 1 (installation script)**
Use the installation script available [here](http://blazingk.in/install_blz_macos.sh). (Always read scripts you download before running them).

**Option 2 (manual)**

1.) Install Java

2.) Clone the blz-ospl project from github

3.) Add the blz-ospl 'bin' folder to your path

`echo 'export PATH=$PATH:INSTALLDIRECTORY/bin' >> ~/.bash_profile`

Where INSTALLDIRECTORY is the directory where you saved blz-ospl

4.) Reload your bash profile

`. ~/.bash_profile`

5.) From the terminal, run

`blz -h`

## Docker

The blz language is available as a docker image in the [blzlang/blz dockerhub repository](https://hub.docker.com/r/blzlang/blz/)

If you have docker already installed on your system, it is easy to try out!

**To run interactive mode**

1.) `docker run -it blzlang/blz -i`

**To create a docker image**

1.) Create a dockerfile `FROM blzlang/blz`

2.) Setup dockerfile as normal

3.) Use `RUN blz YourFile.blz` or `CMD blz YourFile.blz`