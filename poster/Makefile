.PHONY : clean cleanpdf cleandist all poster.pdf

TARGET=poster

all: poster.pdf clean

poster.pdf: $(wildcard *.tex) $(wildcard *.bib)
	- pdflatex -halt-on-error -shell-escape $(TARGET)
	- bibtex  $(TARGET)
	pdflatex -halt-on-error -shell-escape $(TARGET)

clean:
	rm -f *.eps
	rm -f *.aux *.log *.out *.bbl *.blg *~ *.bak $(TARGET).ps
	rm -f *.brf *.lof *.lot *.toc *.glo *.ist
	rm -rf _minted-$(TARGET) .auctex-auto

cleanpdf:
	rm -f $(TARGET).pdf

cleandist: clean cleanpdf
