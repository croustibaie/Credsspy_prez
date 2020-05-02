INCLUDES=

STY_FILES=$(wildcard *.sty)
TEX_SRC=$(wildcard *.tex)
PDF_FROM_TEX=$(TEX_SRC:%.tex=%.pdf)

CC=pdflatex -halt-on-error #-interaction=batchmode

all: $(PDF_FROM_TEX)

%.pdf: %.tex $(STY_FILES) $(INCLUDES)
	$(CC) $<
	$(CC) $<

clean:
	@rm -f $(PDF_FROM_TEX)
	@rm -f *.log *.aux *.out *.dvi *.toc *.nav *.vrb *.snm
