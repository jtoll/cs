# Install TeX on Mac

Notes for a minimum installation of TeX on Mac OS for [R](https://www.r-project.org) package development.

### 1) Download [BasicTeX](http://www.tug.org/mactex/morepackages.html), a smaller version of the full [MacTex](http://www.tug.org/mactex/).
While the usage of the basic version will require the installation of additional fonts, the benefit is a greater than 90% decrease in size.  The installation package for the full version of MacTeX is approximately 2GB, while the basic installation package is only 112MB.

### 2) Update TeX packages
After BasicTeX installation, update to the latest version of each package.
<small>*Note: The use of `sudo` for updating and package installation may be required.*</small>

```
sudo tlmgr update --self
sudo tlmgr update --all
```

### 3) Install additional fonts
To fix errors, when checking R packages, resulting from the absence of the ***inconsolata*** and ***Metric*** fonts.  Install the `collection-fontsrecommended` and `inconsolata` packages.  The `collection-fontsrecommended` package is a pseudo-package which installs 29 font packages.

```
sudo tlmgr install collection-fontsrecommended
sudo tlmgr install inconsolata
```

### Additional examples
List all possible packages:
```
tlmgr list
```

List only installed packages:
```
tlmgr list --only-installed
```

Get information about a particular package:
```
tlmgr info collection-fontsrecommended
```

Search package descriptions for a particular word or phrase:
```
tlmgr list | grep 'Base 35'
```

### References

<https://stat.ethz.ch/pipermail/r-devel/2013-June/066850.html>  
<https://www.ctan.org/pkg/inconsolata>  
<https://www.tug.org/texlive/>
