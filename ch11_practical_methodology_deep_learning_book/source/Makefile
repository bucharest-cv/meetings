# Prerequisites:
GRAPHICS   = $(wildcard ./graphics/*.png)
NOTES      = notes
SLIDES     = slides
REFERENCES = references

.PHONY: all clean release

all : $(NOTES).pdf $(SLIDES).pdf

release : all
	@mv $(NOTES).pdf $(SLIDES).pdf ../release

clean:
	@rm -f *.aux *.bbl *.blg *.log *.out *.nav *.snm *.pdf
	@echo clean done

notes.pdf : $(NOTES).tex $(REFERENCES).bib
	pdflatex $(NOTES)
	bibtex   $(NOTES)
	pdflatex $(NOTES)
	pdflatex $(NOTES)

slides.pdf : $(SLIDES).tex $(REFERENCES).bib
	pdflatex $(SLIDES)
	bibtex   $(SLIDES)
	pdflatex $(SLIDES)
	pdflatex $(SLIDES)


