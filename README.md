# Project 128

## How to install?

``` bash
# Clone repository
$ git clone https://github.com/stefanwimmer128/proj128.git

# Install Project 128
$ ./proj128 install

# or with custom bin folder (default: /usr/bin)
$ ./project install ~/.bin
```

## How to use?

Create a file that contains all the scripts. For example:

``` bash
VERSION="1.0.0-alpha.0"

function install()
{
    local dist="$(readlink -f "${1:-/usr/bin}")/proj128"
    [ -f "$dist" ] && rm "$dist"
    cp "proj128" "$dist"
    sed -i "s#\${VERSION}#$VERSION#" "$dist"
}

function test()
{
    if ./proj128 check 0 && ! ./proj128 check 1
    then
        echo "Test ok"
    else
        echo "Test failed"
        return 1
    fi
}

function check()
{
    return $1
}
```

Then run a script using the `proj128` command.

``` bash
$ proj128 install ~/.bin
```
