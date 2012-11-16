# Makefile | CS 6260 - "Vendetta" Proposal

MAIN=proposal
BIB=sources

pdfonly: $(MAIN).tex $(BIB).bib
	pdflatex -shell-escape $(MAIN) \
		&& bibtex $(MAIN) \
		&& pdflatex -shell-escape $(MAIN) \
		&& pdflatex -shell-escape $(MAIN) \

pdfview: $(MAIN).tex $(BIB).bib
	pdflatex -shell-escape $(MAIN) \
		&& bibtex $(MAIN) \
		&& pdflatex -shell-escape $(MAIN) \
		&& pdflatex -shell-escape $(MAIN) \
		&& open $(MAIN).pdf

view: $(MAIN).pdf
	open $(MAIN).pdf

clean:
	rm -f $(MAIN).aux $(MAIN).pyg $(MAIN).bbl $(MAIN).blg $(MAIN).log $(MAIN).out $(MAIN).pdf

edit:
	$(EDITOR) $(MAIN).tex $(BIB).bib

live:
	latexmk -pdf -pvc $(MAIN) &>/dev/null &
	$(EDITOR) $(MAIN).tex $(BIB).bib

