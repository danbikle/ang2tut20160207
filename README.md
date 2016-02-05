hello world

The purpose of this repo is to help me walk through the Angular2 tutorial which is listed here:

https://angular.io/docs/ts/latest/tutorial/

I prefer to use Ubuntu 14.04 because it runs on both my laptop and on Amazon.

I start by installing Ubuntu 14.04 on my laptop.

The most recent version of Ubuntu which I like is at this URL:

http://releases.ubuntu.com/14.04.3/ubuntu-14.04.3-desktop-amd64.iso

The three general paths to install Ubuntu on a laptop are listed below:

- Remove Windows and install Ubuntu
- Ignore Windows and install Ubuntu on USB drive
- Install VirtualBox on Mac or Windows, Install Ubuntu inside VirtualBox

My favorite path is path2: Ignore Windows and install Ubuntu on USB drive.

Path2 works well with a new laptop should I want to maintain the warranty.

If you are new to the world of Ubuntu laptops I suggest you buy a cheap windows laptop from Walmart and run some experiments.

E-me if you need help: bikle101@gmail.com

When I install Ubuntu, it will ask who I am.

I tell Ubuntu that my name is ann.

Then, Ubuntu will create an account named ann which has useful privileges.

If you use a different initial account, you should create an account named ann after you boot the laptop.

The shell commands to create the ann account are listed below:
```bash
sudo useradd -m -s /bin/bash ann
sudo passwd ann
```

The first command creates ann.
The second command gives her a password.

After I create the ann account, I enhance and update Ubuntu.

The shell commands to do this are listed below:

```bash
sudo apt-get update
sudo apt-get upgrade

sudo apt-get install autoconf bison build-essential libssl-dev libyaml-dev \
libreadline6-dev zlib1g-dev libncurses5-dev libffi-dev libgdbm3 sqlite3    \
libgdbm-dev libsqlite3-dev gitk emacs wget curl openssh-server aptitude

sudo apt-get update
sudo apt-get upgrade
```

After that I login as ann and I download Node.js.

wget https://nodejs.org/dist/v5.5.0/node-v5.5.0-linux-x64.tar.gz

Then I install it:
```bash
rm -rf  node
tar zxf node-v5.5.0-linux-x64.tar.gz
mv      node-v5.5.0-linux-x64 node
```

So, I did that on my laptop.

Then I did this:
```bash
cd ~ann
git clone https://github.com/danbikle/ang2tut20160207
cd  ang2tut201602
npm install
npm start
```
