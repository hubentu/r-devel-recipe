# R-devel conda recipe
* Forked from [r-base-feedstock](https://github.com/conda-forge/r-base-feedstock.git).
* Compiled on macOS 10.15.3

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

Or just install the compiled version from ubuntu 18.04
```sh
conda install --use-local r-devel-4.0.0-hbba0a16_1.tar.bz2
conda install libopenblas 
```

* Use R 4.0
```sh
conda activate r-devel
R --version
```

