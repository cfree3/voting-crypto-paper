# Makefile | CS 6260 - "Vendetta" Proposal

MAIN=proposal
BIB=sources

pdfonly: $(MAIN).tex $(BIB).bib
	pdflatex $(MAIN) && bibtex $(MAIN) && pdflatex $(MAIN) && pdflatex $(MAIN)

pdfview: $(MAIN).tex $(BIB).bib
	pdflatex $(MAIN) && bibtex $(MAIN) && pdflatex $(MAIN) && pdflatex $(MAIN) && open $(MAIN).pdf

view: $(MAIN).pdf
	open $(MAIN).pdf

clean:
	rm -f $(MAIN).aux $(MAIN).pyg $(MAIN).bbl $(MAIN).blg $(MAIN).log $(MAIN).out $(MAIN).pdf

edit:
	$(EDITOR) $(MAIN).tex $(BIB).bib

live:
	latexmk -pdf -pvc $(MAIN) &>/dev/null &
	$(EDITOR) $(MAIN).tex $(BIB).bib

