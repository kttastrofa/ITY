# name:		Makefile for project 1, ITY
# author: 	Katarína Mečiarová
#=======================================================================================================================


PROJECT = 'latex_and_Makefile'
MAIN = proj1
TEX_SOURCES = Makefile \
              $(MAIN).tex


all: $(MAIN).pdf


$(MAIN).pdf: $(TEX_SOURCES) $(FIGURES)
	pdflatex $(MAIN)


clean:
	-rm -f $(MAIN).{pdf,log,blg,bbl,aux,out,toc,idx,bcf,run.xml,ind,ilg,fls,fdb_latexmk} final.pdf

	pdflatex $(MAIN)


.PHONY: clean all
