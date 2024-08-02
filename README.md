# key lab environment modules

## Usage

### Pre-requisites

Ensure the following are in your `.bashrc`

```bash
export MODULE_BASEDIR="/path/to/lab/basedir"
export MPCDF_DISABLE_MODULE_AVAIL_HINT=1
module use --append /path/to/shared/Modules/modulefiles
```

### Usage

```bash
module avail phylip
module load phylip
```

## Useful

[MPCDF docs](https://docs.mpcdf.mpg.de/doc/computing/software/environment-modules.html)