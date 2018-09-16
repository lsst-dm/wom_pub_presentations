#
#

SRC=$(wildcard DM-*.tex)
tex=$(filter-out $(wildcard *acronyms.tex) , $(wildcard *.tex))  

OBJ=$(SRC:.tex=.pdf)

all: $(OBJ)

$(OBJ): %.pdf : %.tex   *tex
	latexmk -bibtex -xelatex -f $<

clean :
	latexmk -c
	rm *.pdf

acronyms.tex :$(tex) myacronyms.txt
	python3 ${TEXMFHOME}/../bin/generateAcronyms.py   $(tex)

