#
#


SRCS=$(wildcard *.tex)

OBJS=$(SRCS:.tex=.pdf)

all: WOM-DM-Status.pdf 

WOM-DM-Status.pdf:${SRCS}

TEX=WOM-DM-Status.tex 
acronyms.tex: ${TEX}
	acronyms.csh  ${TEX}

%.pdf: %.tex 
	latexmk -bibtex -pdf  -f  $<

clean :
	latexmk -c 
	rm *.pdf
