PROJ=proj4
PACK=xjavor20-fit

$(PROJ).pdf: $(PROJ).ps
	ps2pdf -sPAPERSIZE=a4 $(PROJ).ps
$(PROJ).ps: $(PROJ).dvi
	dvips -t a4 $(PROJ).dvi
$(PROJ).dvi: $(PROJ).tex
	latex $(PROJ).tex
	bibtex $(PROJ)
	latex $(PROJ).tex
	latex $(PROJ).tex

$(PACK).tar.gz: $(PROJ).tex
	tar -czf $(PACK).tar.gz Makefile $(PROJ).tex $(PROJ).bib czechiso.bst


tar: $(PACK).tar.gz

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps $(PROJ).blg $(PROJ).bbl

