# name:		Makefile for project 3, ITY
# author: 	Katarína Mečiarová
#=======================================================================================================================


PROJECT = 'latex_and_Makefile'
MAIN = proj3
TEX_SOURCES = Makefile \
              $(MAIN).tex \
                oniisan.eps \
                oniisan2.eps \
                etiopan.eps


all: $(MAIN).pdf


$(MAIN).pdf: $(TEX_SOURCES) $(FIGURES)
	pdflatex $(MAIN)
	makeindex $(MAIN)
	bibtex $(MAIN)
	pdflatex $(MAIN)
	pdflatex $(MAIN)
	@#latexmk -pdf -pvc -pdflatex="pdflatex $(OPT)" $(MAIN)


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
	zip -q $(MAIN).zip $(TEX_SOURCES) proj3.pdf

.PHONY: clean all zip
