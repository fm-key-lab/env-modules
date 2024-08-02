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

### Syncing modules

To update modulefiles on the cluster:

```bash
cd /path/to/shared/Modules/
git pull
```

Set up using:

```bash
cd /path/to/shared/Modules/
git init
git remote add origin https://github.com/fm-key-lab/env-modules.git
git config core.sparseCheckout true
echo "modulefiles/*" >> .git/info/sparse-checkout
git fetch origin main
git checkout -b main
git branch --set-upstream-to=origin/main main
```

## Useful

[MPCDF docs](https://docs.mpcdf.mpg.de/doc/computing/software/environment-modules.html)