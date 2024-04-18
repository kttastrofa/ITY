PROJECT = 'latex_and_Makefile'
MAIN = proj4
TEX_SOURCES = Makefile \
              $(MAIN).tex \
              $(MAIN).bib

FIGURES := $(shell find images/* -type f)

SHELL=/bin/bash
DATE = $(shell date +"%d%b%Y")
OPT = --interaction=nonstopmode

all: $(MAIN).pdf


$(MAIN).pdf: $(TEX_SOURCES) $(FIGURES)
	pdflatex $(OPT) $(MAIN)
	makeindex $(OPT) $(MAIN)
	bibtex $(MAIN)
	pdflatex $(OPT) $(MAIN)
	pdflatex $(OPT) $(MAIN)
	pdflatex $(OPT) $(MAIN)
	pdflatex $(OPT) $(MAIN)
	@#latexmk -pdf -pvc -pdflatex="pdflatex $(OPT)" $(MAIN)


once:
	pdflatex $(MAIN)

clean:
	-rm -f $(MAIN).{pdf,log,blg,bbl,aux,out,toc,idx,bcf,run.xml,ind,ilg,fls,fdb_latexmk} final.pdf

	pdflatex $(MAIN)
	makeindex $(MAIN)
	bibtex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)
	@#latexmk -pdf -pvc -pdflatex="pdflatex $(OPT)" $(MAIN)
zip:
	$(MAKE) clean
	$(MAKE) all
	$(MAKE) clean
	zip -q $(MAIN).zip $(TEX_SOURCES) $(FIGURES) proj3.pdf

.PHONY: clean all
