# GIT multi

The most stupid way to run a git command on multiple repositories.


## Install

```npm install git-multi```


## Setup

 1. ```cd <main repository>```
 2. create ```.gitmulti``` file
 3. add to ```.gitmulti``` the path to any repository you want to manage with git-multi (1 per line)


## Example

If you have the following repositories:
```
/workspace/main-app
/workspace/lib-1
/workspace/lib-2
```

You can configure git-multi on your ```main-app```:
*/workspace/main-app/.gitmulti*
```
../lib-1
../lib-2
```

And then run a git command to your repositories:
```
cd /workspace/main-app
git multi status
```
