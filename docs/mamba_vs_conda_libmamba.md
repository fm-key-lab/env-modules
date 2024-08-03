# Comparing `mamba` with `conda` using the `solver: libmamba`

In December 2022, `libmamba` replaced the "classic" environment solver as the default for `conda` (see [`conda-libmamba-solver` v22.12.0 release notes](https://github.com/conda/conda-libmamba-solver/releases/tag/22.12.0)). Nevertheless, `mamba` will still be faster than `conda` due to other differences, which you can start to read about [here](https://github.com/conda/conda-libmamba-solver/issues/227).

Therefore, MPCDF's `anaconda` modules will be slower at solving environments than `[micro]mamba`. You can confirm which solver is used by inspecing the config file, for instance for the `conda` provided by module `anaconda/3/2023.03`:

```bash
$ cat /mpcdf/soft/SLE_15/packages/x86_64/anaconda/3/2023.03/.condarc
solver: libmamba
envs_dirs:
  - ~/conda-envs
channels:
  - conda-forge
```

## Links

- [Administering a multi-user conda installation](https://conda.io/projects/conda/en/latest/user-guide/configuration/admin-multi-user-install.html)
- [`conda-libmamba-solver`: User Guide](https://conda.github.io/conda-libmamba-solver/user-guide/)