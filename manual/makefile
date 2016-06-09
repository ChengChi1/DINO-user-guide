SHELL=/bin/sh
filename=dinosoars_manual_v0
main =$(filename).tex
bibf =$(filename).aux
refer = chapters/references.bib
default: pdf
all: pdf

.IGNORE:

pdf: $(main:.tex=.pdf)

clean:
	/bin/rm -f $(main:.tex=.aux)
	/bin/rm -f $(main:.tex=.bbl)
	/bin/rm -f $(main:.tex=.blg)
	/bin/rm -f $(main:.tex=.log)
	/bin/rm -f $(main:.tex=.spl)
	/bin/rm -f $(main:.tex=.ps) 
	/bin/rm -f $(main:.tex=.dvi) 
	/bin/rm -f $(main:.tex=.out) 
	/bin/rm -f $(main:.tex=.synctex.gz*) 
	/bin/rm -f chapters/*.aux

cleanall:
	/bin/rm -f $(main:.tex=.aux)
	/bin/rm -f $(main:.tex=.bbl)
	/bin/rm -f $(main:.tex=.blg)
	/bin/rm -f $(main:.tex=.log)
	/bin/rm -f $(main:.tex=.spl)
	/bin/rm -f $(main:.tex=.pdf) 
	/bin/rm -f $(main:.tex=.ps) 
	/bin/rm -f $(main:.tex=.dvi) 
	/bin/rm -f $(main:.tex=.out) 
	/bin/rm -f $(main:.tex=.synctex.gz*) 
	/bin/rm -f chapters/*.aux

$(main:.tex=.pdf): $(main)
	latex $(main)
	bibtex $(main:.tex=.aux)
	latex $(main)
	latex $(main)
	dvips $(main:.tex=.dvi)
	ps2pdf $(main:.tex=.ps)
