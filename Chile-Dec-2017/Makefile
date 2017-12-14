#
#


SRCS=$(wildcard *.tex)

OBJS=$(SRCS:.tex=.pdf)

all: WOM_DM_DEC_2017.pdf WOM_DM_LSP_2017.tex

WOM_DM_DEC_2017.pdf:${SRCS}
WOM_DM_LST_2017.pdf:${SRCS}

TEX=WOM_DM_DEC_2017.tex dm.tex lsst.tex conclusion.tex sciplat*tex wod.tex docs.tex dmchal.tex ops.tex lssthistory.tex
acronyms.tex: ${TEX}
	acronyms.csh  ${TEX}

%.pdf: %.tex 
	latexmk -bibtex -pdf  -f  $<

clean :
	latexmk -c 
	rm *.pdf
