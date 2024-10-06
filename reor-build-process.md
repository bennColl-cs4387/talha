First I forked the repo [here](https://github.com/mdtalhachy/reor-mtc).

For starter I wanted to clone and build the original [repo](https://github.com/reorproject/reor). To accomplish that, I've created a folder in my drive and named it "reor-contributions". Then I've proceeded to clone the repo inside that folder by running:

```git clone https://github.com/reorproject/reor.git```

After it was cloned successfully, I've run the following command to install the necessary dependencies: 

```npm install```

I've received the following error after running that ```npm install```: 

```
npm ERR! code ENOENT
npm ERR! syscall open
npm ERR! path /Users/talhachy/Documents/Class Documents/Open-Source-Software-Building/reor-contributions/package.json
npm ERR! errno -2
npm ERR! enoent ENOENT: no such file or directory, open '/Users/talhachy/Documents/Class Documents/Open-Source-Software-Building/reor-contributions/package.json'
npm ERR! enoent This is related to npm not being able to find a file.
npm ERR! enoent 

npm ERR! A complete log of this run can be found in: /Users/talhachy/.npm/_logs/2024-10-06T17_55_12_634Z-debug-0.log

```
