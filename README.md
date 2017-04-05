# proj128

Project 128 - Project Manager

## How to install?

``` bash
$ curl https://raw.githubusercontent.com/stefanwimmer128/proj128/v1-dev/install | bash

$ yarn (global) add proj128

$ npm i (-g) proj128
```

## How to use?

Create a file that contains all the scripts. For example:

``` bash
function doSomething()
{
    echo "doSomething $@"
}
```

Then run a script using the `proj128` command.

``` bash
$ proj128 doSomething some params
```
