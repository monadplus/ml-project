.PHONY : clean cleanpdf cleandist all

TARGET=main

all: main.pdf clean

main.pdf: $(wildcard *.tex) $(wildcard *.bib)
	- bibtex  bibligraphy.bib
	pdflatex -halt-on-error -shell-escape $(TARGET)

clean:
	rm -f *.eps
	rm -f *.aux *.log *.out *.bbl *.blg *~ *.bak $(TARGET).ps
	rm -f *.brf *.lof *.lot *.toc *.glo *.ist
	rm -rf _minted-$(TARGET) .auctex-auto

cleanpdf:
	rm -f $(TARGET).pdf

cleandist: clean cleanpdf
