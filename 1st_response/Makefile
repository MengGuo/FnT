LATEXMK ?= latexmk
SOURCE := author_response.tex
LATEXMK_FLAGS := -pdf -synctex=1 -interaction=nonstopmode -halt-on-error -file-line-error

.PHONY: compile follow clean

compile:
	$(LATEXMK) $(LATEXMK_FLAGS) $(SOURCE)

follow:
	$(LATEXMK) $(LATEXMK_FLAGS) -pvc $(SOURCE)

clean:
	$(LATEXMK) -pdf -c $(SOURCE)
