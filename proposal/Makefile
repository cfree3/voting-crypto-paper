# Makefile | CS 6260 - "Vendetta" Proposal

MAIN=proposal
BIB=sources
LATEX=pdflatex -file-line-error -halt-on-error

$(MAIN).pdf: $(MAIN).tex $(BIB).bib
	$(LATEX) $(MAIN) && bibtex $(MAIN) && $(LATEX) $(MAIN) && $(LATEX) $(MAIN)

open: $(MAIN).pdf
	open $(MAIN).pdf

clean:
	rm -f $(MAIN).aux $(MAIN).pyg $(MAIN).bbl $(MAIN).blg $(MAIN).log $(MAIN).out $(MAIN).pdf

edit:
	$(EDITOR) $(MAIN).tex $(BIB).bib

live:
	latexmk -pdf -pvc $(MAIN) &>/dev/null &
	$(EDITOR) $(MAIN).tex $(BIB).bib
