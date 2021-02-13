# rmdyna

Perl script to purge LS-DYNA working directories.

## Installation

Use the following command to install this software:

```bash
$ make
$ make install
```

The default `PREFIX` is set to `/usr/local`.  In order to succesfully complete the installation, you need to have write permissions for the installation location.

## Usage

Use the following command to invoke the script:

```bash
$ rmdyna [--dir PATH] [--mask REGEX] [--force]  [--copy] [--help]
```

### Options

+ `-d`, `--dir=PATH`

  changes the current working directory.

+ `-m`, `--mask=REGEX`

  specifies a comma-separated list of regular expressions to be added to the list of known LS-DYNA output files to search for.  Known LS-DYNA output files are:

  - `abstat`
  - `adptmp`
  - `bg_switch`
  - `binout`
  - `bndout`
  - `bnfile.tmp`
  - `d3dump`
  - `d3hsp`
  - `d3kil`
  - `d3plot`
  - `d3thdt`
  - `disk8`
  - `defgeo`
  - `deforc`
  - `disk8`
  - `dyna.str`
  - `elout`
  - `gceout`
  - `glstat`
  - `intforc`
  - `kill_by_pid`
  - `ldcrvv`
  - `lspost.cfile`
  - `lspost.db`
  - `lspost.msg`
  - `matsum`
  - `messag`
  - `nasbdf`
  - `nodfor`
  - `nodout`
  - `nohup.out`
  - `part_des`
  - `rbdout`
  - `rcforc`
  - `runrsf`
  - `rwforc`
  - `sbtout`
  - `secforc`
  - `sleout`
  - `slsbdf`
  - `spooles.res`
  - `status.out`

+ `-f`, `--force`

  suppresses interactive mode.  

+ `-c`, `--copy`

  creates a directory named by the current data and time and moves all target files found to this directory instead of deleting them.  Backup copies of all remaining files in the working directory are included.

+ `--help`

## Description

This script parses a LS-DYNA working directory for output files and removes them.  The identified target files can either be moved to a backup directory or removed permanently.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
