# GIT multi

The most stupid way to run a git command on multiple repositories.


## Install

Install this library via [NPM](https://www.npmjs.org/package/git-multi):
``` bash
npm -g install git-multi
```


## How it works

`git-multi` runs a git command sequentially on 2+ repositories. This can be useful when you have a project spread on more repositories (ie. an app repository and some dependencies, like libraries or plugins) and you want to run the same exact git command on the main repository and it dependencies.


## Setup

 1. ```cd <main repository>```
 2. create `.gitmulti` file
 3. add to `.gitmulti` the path to any repository you want to manage with git-multi (1 per line)

Then, in the `<main repository>` you can run any git command like this:
``` bash
git multi status
```

And it will run ```git status``` in the `<main repository>` and all dependencies repositories (configured in `.gitmulti`).


## Example

If you have the following repositories:
```
/workspace/main-app
/workspace/lib-1
/workspace/lib-2
```

You can configure git-multi on your ```main-app```:
```
echo "../lib-1" >> /workspace/main-app/.gitmulti
echo "../lib-2" >> /workspace/main-app/.gitmulti
```

And then run:
``` bash
cd /workspace/main-app
git multi status
```
