### Building from the Source Repo

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

After some debugging turns out that I've run ```npm install``` in the wrong directory. I should've cd'ed into the directory of the cloned repo. Once I did that and run it again, it was successful. 

Next, I went onto building the project running the following command: 

```npm run build```

It took a while to build but the build went sucessful. 


### Building from My Forked Repo

I went through the same process of cloning except changing the URL of the target repo from source repo to my forked repo. Then I've run the ```npm install``` to install the dependencies. Then I've run ```npm run build``` once just to make sure everything builds correctly before I start changing something. The build went successful.  

For changing something, I wanted to make a quick small change just to see if I can get through the process of changing and building. So I chose to change the following sentence in the readme from "Make sure you have nodejs installed." to "Make sure you have nodejs installed on your computer."

What I've noticed that, once I run the ```git commit", the project automatically runs some checks and builds the project to make sure everything went alright. So I'd say changing and building from source went successful as well. Here's the log for reference: 

```
git commit -m "Changed slight wording"

Running some lint checks on your (hopefully) beautiful code...


> reor-project@0.2.21 lint:fix
> eslint . --ext .ts,.tsx --fix


warn - The class `delay-[400ms]` is ambiguous and matches multiple utilities.
warn - If this is content and not a class, replace it with `delay-&lsqb;400ms&rsqb;` to silence this warning.

warn - The class `delay-[400ms]` is ambiguous and matches multiple utilities.
warn - If this is content and not a class, replace it with `delay-&lsqb;400ms&rsqb;` to silence this warning.

> reor-project@0.2.21 type-check
> tsc && vite build

vite v4.5.2 building for production...
transforming (48) node_modules/@sentry/browser/build/npm/esm/tracing/reques
warn - The class `delay-[400ms]` is ambiguous and matches multiple utilities.
warn - If this is content and not a class, replace it with `delay-&lsqb;400ms&rsqb;` to silence this warning.
✓ 5513 modules transformed.
dist/index.html                     0.83 kB │ gzip:   0.45 kB
dist/assets/index-01af6837.css     61.61 kB │ gzip:  11.35 kB
dist/assets/index-3aedc415.js   2,922.74 kB │ gzip: 858.21 kB

(!) Some chunks are larger than 500 kBs after minification. Consider:
- Using dynamic import() to code-split the application
- Use build.rollupOptions.output.manualChunks to improve chunking: https://rollupjs.org/configuration-options/#output-manualchunks
- Adjust chunk size limit for this warning via build.chunkSizeWarningLimit.
✓ built in 18.87s
vite v4.5.2 building for production...
✓ 972 modules transformed.
dist-electron/main/index.js             0.66 kB │ gzip:   0.26 kB
dist-electron/main/index-973b8207.js   37.26 kB │ gzip:   8.44 kB
dist-electron/main/index-f55efb07.js  415.72 kB │ gzip: 126.10 kB
✓ built in 2.00s
vite v4.5.2 building for production...
✓ 1 modules transformed.
dist-electron/preload/index.js  3.48 kB │ gzip: 1.21 kB
✓ built in 15ms
[main 3180858] Changed slight wording
 1 file changed, 1 insertion(+), 1 deletion(-)

```




