# Makefile | CS 6260 - "Vendetta" Notes

MAIN=paper
BIB=sources
LATEX=latexmk -pdf

$(MAIN).pdf: $(MAIN).tex $(BIB).bib
	$(LATEX) $(MAIN)

open: $(MAIN).pdf
	open $(MAIN).pdf

clean:
	$(LATEX) -C

edit:
	$(VISUAL) $(MAIN).tex $(BIB).bib

live:
	$(LATEX) -pvc $(MAIN) &>/dev/null &
	$(VISUAL) $(MAIN).tex $(BIB).bib
