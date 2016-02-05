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
cd  ang2tut20160207
npm install
npm start
```

The console indicated that lite-server was serving at two URLs:

http://localhost:3000

http://localhost:3001

The first URL corresponded to my Angular2 app.

The second URL corresponded to an admin-UI for lite-server.

I saw this:
```bash
ann@nia111:~/ang2tut20160207 $ npm start

> angular2-quickstart@1.0.0 start /home/ann/ang2tut20160207
> concurrent "npm run tsc:w" "npm run lite" 

[1] 
[1] > angular2-quickstart@1.0.0 lite /home/ann/ang2tut20160207
[1] > lite-server
[1] 
[0] 
[0] > angular2-quickstart@1.0.0 tsc:w /home/ann/ang2tut20160207
[0] > tsc -w
[0] 
[1] [BS] Access URLs:
[1]  ----------------------------------
[1]        Local: http://localhost:3000
[1]     External: http://10.0.2.15:3000
[1]  ----------------------------------
[1]           UI: http://localhost:3001
[1]  UI External: http://10.0.2.15:3001
[1]  ----------------------------------
[1] [BS] Serving files from: ./
[1] [BS] Watching files...
[0] 8:02:19 AM - Compilation complete. Watching for file changes.
[1] [BS] File changed: app/hero.js
[1] [BS] File changed: app/hero-detail.component.js
[1] [BS] File changed: app/mock-heroes.js
[1] [BS] File changed: app/hero.service.js
[1] [BS] File changed: app/app.component.js
[1] [BS] File changed: app/main.js
[1] 16.02.05 08:02:20 304 GET /./index.html (Unknown - 32ms)
[1] 16.02.05 08:02:21 304 GET /app/main.ts (Unknown - 13ms)
[1] 16.02.05 08:02:21 304 GET /app/app.component.ts (Unknown - 33ms)
[1] 16.02.05 08:02:22 404 GET /favicon.ico (Unknown - 23ms)
[1] 16.02.05 08:02:22 304 GET /app/hero-detail.component.ts (Unknown - 7ms)
[1] 16.02.05 08:02:22 304 GET /app/hero.service.ts (Unknown - 7ms)
[1] 16.02.05 08:02:22 304 GET /app/mock-heroes.ts (Unknown - 58ms)
```

Also it brought up a browser and displayed the same content I saw at this URL:

https://angular.io/resources/live-examples/toh-4/ts/plnkr.html

So, that convinced me I was on the right track.

Next, I removed some files so I could start the tutorial:
```bash
cd ~/ang2tut20160207/
rm index.html
rm -rf app
mkdir  app
```

Then, by hand, I copied in the three files from this URL:

https://angular.io/resources/live-examples/quickstart/ts/plnkr.html

Next, I followed the tutorial at this URL:

https://angular.io/docs/ts/latest/tutorial

If you have questions, e-me: bikle101@gmail.com

