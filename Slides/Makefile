
LECTURES := L01 L02 L03 L04 L05 L06 L07 L08 L09 L10 L11 L12 L13 L14 L15 L16 L17 L18 L19 L20 L21 L22
LABS := Lab0 Lab1p1 Lab1p2 Lab3p1

TEXINPUTS := mtheme/:$(TEXINPUTS)

STYS_FILES := beamercolorthememetropolis-highcontrast.sty \
			beamercolorthememetropolis.sty \
			beamerfontthememetropolis.sty \
			beamerinnerthememetropolis.sty \
			beamerouterthememetropolis.sty \
			beamerthememetropolis.sty \
			pgfplotsthemetol.sty

STYS := $(addprefix mtheme/,$(STYS_FILES))

all: $(LECTURES) $(LABS)

$(STYS):
	cd mtheme && make

dep: $(STYS)

lectures: $(LECTURES) $(STYS)

labs: $(LABS) $(STYS)

.PHONY: clean

clean: 
	latexmk -c

clean_pdf:
	latexmk -C

%: %.tex
	latexmk -xelatex $@
