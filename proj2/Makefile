PROJ=proj2
PACK=xjavor20-fit

.PHONY: clean pack pdflatex

pdf:
	pdflatex $(PROJ).tex
	pdflatex $(PROJ).tex

$(PACK).tar.gz: $(PROJ).tex
	tar -czf $(PACK).tar.gz Makefile $(PROJ).tex

tar: $(PACK).tar.gz

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps
