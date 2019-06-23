#
#

SRC=$(wildcard WOM-*.tex)
tex=$(filter-out $(wildcard *acronyms.tex) , $(wildcard *.tex))  

OBJ=WOM_BD_ASTRO.pdf

all: $(OBJ) 

$(OBJ): %.pdf : %.tex $(tex)
	latexmk -bibtex -xelatex -f $<

clean :
	latexmk -c
	rm *.pdf

acronyms.tex :$(tex) myacronyms.txt
	generateAcronyms.py   $(tex)

