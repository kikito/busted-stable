# busted-stable rock

Easily install a stable version of [busted](http://olivinelabs.com/busted/)

## Prerequisites

Install luarocks.

## Installation

    $ luarocks install busted-stable

That will install a working version of busted. You don't need to remember 1.11.1-1 or cliargs versions.

## Why?

As of the time of this writing, the busted version in luarocks is unstable, and it has been for ~300 days.

This means that if you installed it with:

    $ luarocks install busted

You got a broken version of the rock (and you have gotten that for the last 300 days or so).

The solution used to be installing an older version of busted:

    $ luarocks install busted 1.11.1-2

Unfortunately, this has stopped being enough. Recently [the stable version of busted was broken by a non-backwards compatible update in lua_cliargs](https://github.com/Olivine-Labs/busted/issues/391).

So now, in order to get a working `busted` command, you have to install an older version of `lua_cliargs` too:

    $ luarocks install lua_cliargs 2.3-3
    $ luarocks install busted 1.11.1-2

I eventually grew tired of all this, so I have created this rock. It allows you to do this instead:

    $ luarocks install busted-stable

Have a good day!

