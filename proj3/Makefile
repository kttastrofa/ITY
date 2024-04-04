# K suboru: proj3.tex
# K suboru: proj3.tex
# Datum:    03.04.2024
# Autor:    Katarina Meciarova (xmeciak00)
# Projekt:  ITY projekt 2

PROJ=proj3

$(PROJ).pdf: $(PROJ).tex
	latex $(PROJ).tex
	latex $(PROJ).tex
	dvips -t a4 $(PROJ).dvi
	ps2pdf $(PROJ).ps

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps $(PROJ).out

clean-all: clean
	rm -f $(PROJ).pdf
