PROJECT = 'latex_and_Makefile'
MAIN = proj4
TEX_SOURCES = Makefile \
              $(MAIN).tex \
              $(MAIN).bib

SHELL=/bin/bash
DATE = $(shell date +"%d%b%Y")

all: $(MAIN).pdf


$(MAIN).pdf: $(TEX_SOURCES)
	pdflatex $(MAIN).tex
	bibtex $(MAIN).aux
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex
	@#latexmk -pdf -pvc -pdflatex="pdflatex $(OPT)" $(MAIN)


once:
	pdflatex $(MAIN)

clean:
	-rm -f $(MAIN).{pdf,log,blg,bbl,aux,out,toc,idx,bcf,run.xml,ind,ilg,fls,fdb_latexmk} final.pdf

	pdflatex $(MAIN).tex
	bibtex $(MAIN).aux
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex
	pdflatex $(MAIN).tex
	@#latexmk -pdf -pvc -pdflatex="pdflatex $(OPT)" $(MAIN)
zip:
	$(MAKE) clean
	$(MAKE) all
	$(MAKE) clean
	zip -q $(MAIN).zip $(TEX_SOURCES) proj4.pdf

.PHONY: clean all zip
