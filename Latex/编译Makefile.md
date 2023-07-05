
```makefile
PROJECTNAME=Physics-High-School
MAKE_PATH=$(abspath $(lastword $(MAKEFILE_LIST)))
SRCPATH=$(dir $(MAKE_PATH))
OUTPATH=$(SRCPATH)out

build:
	latexmk -xelatex -interaction=nonstopmode -synctex=1 -output-directory=$(OUTPATH) $(PROJECTNAME).tex
```