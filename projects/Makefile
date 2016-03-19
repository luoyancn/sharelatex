# Makefile for Sphinx documentation
#

BUILDDIR      = build
BASENAME      = $(notdir $(CURDIR))

help:
	@echo "Please use \`make <target>' where <target> is one of"
	@echo "  latexpdf   to make LaTeX files and run them through pdflatex"

clean:
	rm -rf $(BUILDDIR)/*

echo:
	@echo $(BASENAME)

pdf:
	@echo "Running LaTeX files through xelatex..."
	xelatex -output-directory=$(BUILDDIR) $(BASENAME).tex
	-bibtex $(BUILDDIR)/$(BASENAME).aux
	xelatex -output-directory=$(BUILDDIR) $(BASENAME).tex
	xelatex -output-directory=$(BUILDDIR) $(BASENAME).tex
	@echo "xelatex finished; the PDF files are in $(BUILDDIR)/latex."
