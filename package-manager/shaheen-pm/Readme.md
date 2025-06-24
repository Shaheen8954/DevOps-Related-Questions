🧠 Assignment: Package Manager and some other Topics – DevOps Interview Practice Question's-answer:

What is packge manager?
Package manager is a tool that helps you to install, update,remove, and manage software on your linux system automatically.

Exaple-
You want to coock something, which ingredeint is required to make that recipe instead of purchesing every ingredient from diffrent shop you prefer to go to mall and purchese all ingredient from one place that is package manager.

why it is used?

We use package manager :
To save time  -no need to downloade files manually
To manage dependencies  -it download all files automatically which is required to install that perticular software.
To keep software updated  - package manager not only installs, but also updates and upgrades software.
Secure -downloads packages from trusted sources.
Uninstalls cleanly - it deletes everething related to software ( like libreries, bineries, configs), doesn't leave junk,remove software from system


What is the difference between apt and dpkg?


APT and DPKG both are package manager, we use to install software among of both have some deffrences:
APT:
Apt is a high level, smart package manager 
It fetches packages from online reporisitories.
Automatically downloads dependencies
Keeps system updated.


dpkg = low level package tool
It install .deb files which you have allready downloaded
Does not resolve dependencies - it installs only .deb file, does not care if required dependencies is missing, so that app might be broken or not working.

Often used behind scenes of apt.
if dependencies are missing, you will have to install them manually.


What is the function of the yum and dnf package managers?

Both are package managers, used in RedHat-based systems like:
RHEL ( RedHat Enterprise Linux)
CentOs
Fedora

Function of yum and dnf
install packages
update packages 
Automatically resolve dependencies
remove packages
Search packages
Manage repositories
View package information


Difference between yum and dnf:

Yum is the older whereas dnf is the newer
It's speed is slow,dnf is faster
In handling dependencies yum is weaker whereas dnf is smarter and safer.
It's used in RHEL7, CentOs7, dnf is used in RHEL8 + CentOs8.

dnf is the modern replacement of yum, with more advance features,
Both tools handle installation, updates, resolve dependencies, and removal.



What are .deb and .rpm files in Linux?


They are file installer for linux:
They contains:
The software
the depencies
Instructions to install it.

.deb stands for debian package
used in files stands for debian-based system-
Ubuntu
Debian
Linux mint


.rpm file
.rpm stands for RedHat package
used in redhat-based system like-
RedHat
CentOs
Fedora
Amazon Linux



What is a software repository?hat is a package manager in Linux, and why is it used?



Software repository:

A software repository is a storage location on internet where package are kept.
Each linux distribution (like ubuntu, fedora, etc) has it's own official repos.


What is the difference between apt install and apt-get install?

apt install and apt-get install both are package manager which helps to install packages(software). 
apt-get is the older version which is introduced in 1998.
It is used in script, automation, and backwordcompatability.
Still widely used.
Best for scripts 


apt:
apt is the newer, updated, smarter version,
Introduced in 2014.
Combines features of several older commands( like- apt-get, apt-cache)
gives cleaner output 



How does the package manager resolve dependencies automatically?

First, what are dependencies?
 Dependencies are other software packages that a program needs to work properly.
For exampel:
If you are installing vs code, it might need:
A certain version of node.js
Some fonts
GTK libraries to draw windows
These are it's dependencies.


Now, how does the package manager resolve dependencies automatically:


Step by step process:
run a command
package manager checkes the repository.

The package manager checks your system:

If the required dependency is already installed, it skips it.

If not installed, it adds it to the list.

Step 3: Download All Needed Packages
It downloads nginx and all the missing dependencies from the repository (online server that stores packages).

Step 4: Install in the Right Order
It installs the dependencies first, then installs nginx.

This ensures everything works smoothly.



What happens during sudo apt update under the hood?

Step 1: Check Your sources.list File
Your system looks into /etc/apt/sources.list and /etc/apt/sources.list.d/

These files contain URLs of package repositories (e.g., Ubuntu main, universe, security updates)

Step 2: Contact the Repositories (via Internet)
Your system connects to these servers.

It downloads the latest metadata/index files of all available packages.

This metadata includes:

Package names

Versions

Dependencies

Descriptions

Step 3: Save the Metadata Locally

This local database is what your package manager uses to know:

What packages are available

Which versions exist

What dependencies they need

 Step 4: Compare with Your Current Packages
It doesn’t update the software yet — just compares:

Your current installed package versions

With the latest available ones from the server

So, after apt update, the system knows which packages have newer versions available.

Important Notes:
You should run sudo apt update before installing new software to ensure you're installing the latest version.


How do .repo files work in yum/dnf, and what are their components?


What is a .repo File?
A .repo file is a configuration file that tells yum or dnf where to find software packages (repositories).

How It Works Internally
DNF reads all .repo files in /etc/yum.repos.d/

It contacts the baseurl of each enabled repo

Downloads package metadata (like APT does)

Builds a local cache of available packages








 