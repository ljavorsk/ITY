NAME=proj3
AUTHOR=xjavor20
BUNDLE=etiopan.eps oniisan.eps oniisan2.eps algorithm2e.sty

all: $(NAME).tex
	latex $(NAME).tex
	latex $(NAME).tex
	dvips -t a4 $(NAME).dvi
	ps2pdf -sPAPERSIZE=a4 $(NAME).ps

clean:
	rm $(NAME).aux $(NAME).dvi $(NAME).log $(NAME).pdf $(NAME).ps

zip:
	zip $(AUTHOR)-fit.zip Makefile $(NAME).tex $(BUNDLE)
