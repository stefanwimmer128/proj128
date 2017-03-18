# Project 128

## How to install?

``` bash
# Clone repository
$ git clone https://github.com/stefanwimmer128/proj128.git

# Install Project 128
$ proj128/install
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
