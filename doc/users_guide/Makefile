# Pre-configuration

# Flags for gcc
SOURCES = waterslide_users_guide.tex 

# All C files as sources, and chop off the .c for targets
MODULES = $(patsubst %.tex, %.pdf, $(SOURCES))

all: $(MODULES)

# All targets without an extension depend on their .c files
%.pdf: %.tex
	pdflatex $<
	bibtex waterslide_users_guide
	pdflatex $<
	pdflatex $<

clean:
	@rm -rf *.log *.aux *.bbl *.blg *.out 2> /dev/null

