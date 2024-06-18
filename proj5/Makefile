# name:		Makefile for project 5, ITY
# author: 	Katarína Mečiarová
#=======================================================================================================================

PROJECT = 'latex_and_Makefile'
MAIN = proj5
TEX_SOURCES = 	Makefile \
              	$(MAIN).tex \
              	pic/bayer.jpg \
              	pic/code.png \
              	pic/in.png \
              	pic/meme.jpg \
              	pic/rbt17.png \
              	pic/rot.png \
              	other/references.bib \
              	other/czech.mbs \
              	other/czechiso.bst \
              	other/czechiso.dbj

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
