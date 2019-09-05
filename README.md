# check
Bash script to check the following:

* Domain name availability. TLD defaults: `.com, .io, .net`
* [Twitter](https://twitter.com)
* [GitHub](https://github.com)
* [Instagram](https://instagram.com)

## install

1. Add `check` file to your `PATH`
1. `chmod +x check`

## configuration

By default, the script will check availability of the following TLDs: `.com, .io, .net`

These defaults can be changed by updating the `TLDS` array in the script.

Given an argument `foo`, the script will use `whois` to check domain name availability for: `foo.com, foo.io, foo.net`

`curl` will then be used to check availability of `foo` as a username for: GitHub, Instagram, Twitter

## usage

`check digitalsanctum`

will have output like the following:

```
$ check digitalsanctum
        digitalsanctum.com: TAKEN
         digitalsanctum.io: AVAILABLE
        digitalsanctum.net: AVAILABLE

                    GitHub: TAKEN
                   Twitter: TAKEN
                 Instagram: TAKEN  
```

Tested on Ubuntu 18.04. YMMV
