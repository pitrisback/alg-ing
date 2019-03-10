MAIN_DOC=main
CHAPTERS=$(wildcard chapters/*.tex)

## make all: create pdf
.PHONY : all
all : $(MAIN_DOC).pdf


$(MAIN_DOC).pdf : $(MAIN_DOC).tex $(CHAPTERS)
	pdflatex $<
	pdflatex $<


## clean : remove auto-generated files
.PHONY : clean
clean : 
	rm -f $(MAIN_DOC).aux
	rm -f $(MAIN_DOC).log
	rm -f $(MAIN_DOC).pdf

## variables : print variables used
.PHONY : variables
variables :
	@echo CHAPTERS: $(CHAPTERS)

.PHONY : help
help : makefile
	@sed -n 's/^##//p' $<
