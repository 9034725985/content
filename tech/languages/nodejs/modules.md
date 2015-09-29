---
title: Modules
page: nodejs
order: 2
---

# Modules

## Installation

To install additional modules from Fedora repositories, use:

```
$ sudo dnf install nodejs-<module-name>
```

or 

```
$ sudo dnf install 'npm(module-name)'
```

For example, to install express, you need to type:

```
$ sudo dnf install nodejs-express
```

or 

```
$ sudo dnf install 'npm(express)'
```

Most modules are prefixed with 'nodejs-'. There are, however, a few exceptions (for example mocha), which are not prefixed.

## Using modules

npm allows using require() only on locally installed modules. If you want to require() modules installed by dnf, you need to type:

```
$ npm link express
```

or to load global modules by default, you can set $NODE_PATH as follows: 

```
export NODE_PATH=/usr/lib/node_modules
```

## Missing modules

npm is one of the largest ecosystem of open source libraries in the world and contains thousands of modules and it is impossible to have them all packaged as rpms. However, if you are missing a package and think that it really should be in Fedora repositories, you have several choices:

First one is enabling testing repository. Chances are new modules are already packaged but not yet in stable repositories. To do that, type:

```
dnf config-manager --set-enabled updates-testing
```

to enable testing repository permanently. To use it temporarily, you need to type:

```
yum|dnf install nodejs-<module-name> --enablerepo=updates-testing
```

Second one is joining [Node.js SIG](https://fedoraproject.org/wiki/SIGs/Node.js) and help us improve and provide better software.
