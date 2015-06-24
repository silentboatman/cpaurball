## [deprecated]

Please note that this project is deprecated as of AUR4.
<br><br>

# cpaurball

Tool for submitting source tarballs to the AUR.

## Usage

cpaurball will submit a source tarball located in the current working directory (or specified with the `-a` option) to Arch Linux's AUR.

There are different ways of specifying login credetials to the AUR. It can be specified with the `-u` and `-p` option or by storing them in a config file with the `--configure` option. If non of the these options been used, cpaurball will prompt the user for the information.

By default the same category will be used (if the package already exists in the AUR). This can be overridden with the `-c` option.

```
cpaurball [options]

  -a, --aurball <file>   submits <file> (default: scans current dir)
  -c, --category <name>  sets category to <name> (default: uses the 
                         category of the current uploaded aurball)
      --configure        store login credentials in config
  -h, --help             show this help message and exit
      --nocolor          disable colorized output messages
  -p, --password <pass>  logs in with <pass>
  -V, --version          show version and exit
  -u, --username <name>  logs in with <name>
  -#, --progressbar      show progressbar
```

## Examples

```
$ mkaurball && cpaurball
```
```
$ cpaurball --category "newCategory" --progressbar
```

## License

cpaurball is licensed under GPLv3.
