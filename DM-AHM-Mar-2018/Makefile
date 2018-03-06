#
#


SRCS= welcome.tex ARCH.tex	PIPES.tex WOM-DM-Status.tex goals.tex orstab.tex	 risks.tex DAX.tex SQUARE.tex issues.tex overview.tex NCSA.tex SST.tex conc.tex	miles.tex questions.tex NET.tex	SUIT.tex

OBJS=$(SRCS:.tex=.pdf)

all: WOM-DM-Status.pdf 

WOM-DM-Status.pdf:${SRCS}

TEX=WOM-DM-Status.tex 
acronyms.tex: ${SRCS}
	acronyms.csh  ${SRCS}

%.pdf: %.tex 
	latexmk -bibtex -pdf  -f  $<

clean :
	latexmk -c 
	rm *.pdf
