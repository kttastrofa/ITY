# name:		Makefile for project 5, ITY
# author: 	Katarína Mečiarová
#=======================================================================================================================

PROJECT = 'latex_and_Makefile'
MAIN = proj5
TEX_SOURCES = 	Makefile \
              	$(MAIN).tex \
              	bayer.jpg \
              	code.png \
              	in.png \
              	meme.jpg \
              	rbt17.png \
              	rot.png \
              	references.bib \
              	czech.mbs \
              	czechiso.bst \
              	czechiso.dbj

SHELL=/bin/bash


all: $(MAIN).pdf


$(MAIN).pdf: $(TEX_SOURCES)
	pdflatex $(MAIN)
	bibtex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)
	@#latexmk -pdf -pvc -pdflatex="pdflatex $(OPT)" $(MAIN)


once:
	pdflatex $(MAIN)

clean:
	-rm -f $(MAIN).{pdf,log,blg,bbl,aux,out,toc,idx,bcf,run.xml,ind,ilg,fls,fdb_latexmk} final.pdf

	pdflatex $(MAIN)
	bibtex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)

	@#latexmk -pdf -pvc -pdflatex="pdflatex $(OPT)" $(MAIN)

zip:
	$(MAKE) clean
	$(MAKE) all
	$(MAKE) clean
	zip -q $(MAIN).zip $(TEX_SOURCES) proj4.pdf

.PHONY: clean all zip
