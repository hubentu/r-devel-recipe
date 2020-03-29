# R-devel conda recipe
* Forked from [r-base-feedstock](https://github.com/conda-forge/r-base-feedstock.git).
* Compiled on macOS 10.15.3 and ubuntu 18.04

Add forge channel.
```sh
conda config --add channels conda-forge
```

## Howto
* Create r-devel env
```sh
git clone https://github.com/hubentu/r-devel-recipe.git
cd r-devel-recipe
conda create -n r-devel
conda activate r-devel
```

* Build and install
From source
```sh
conda install conda-build
conda build .
conda install --use-local path/to/r-devel
```

Or just install the compiled version

| System         | R-devel                            |
|----------------|------------------------------------|
| macOS 10.15.3  | `r-devel-4.0.0-hbba0a16_1.tar.bz2` |
| ubuntu 18.04.4 | `r-devel-4.0.0-hd41c036_1.tar.bz2` |

```sh
conda install --use-local r-devel-${version}.tar.gz
# This step might cause Makeconf empty
conda install libopenblas
# install again to fix
conda install --use-local r-devel-${version}.tar.bz2
```

* Use R 4.0
```sh
conda activate r-devel
R --version
```
