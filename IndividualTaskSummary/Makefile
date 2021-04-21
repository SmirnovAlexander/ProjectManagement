SOURCE=lectures_summary.tex
COMPILER=pdflatex
BUILDDIR=build
FLAGS=-shell-escape \
      -interaction nonstopmode \
      -halt-on-error \
      -file-line-error \
      -output-directory=$(BUILDDIR)

all:
	mkdir -p $(BUILDDIR)
	$(COMPILER) $(FLAGS) $(SOURCE)
	mv $(BUILDDIR)/*.pdf .

clean:
	rm -rf $(BUILDDIR) _minted-slides/ indent.log

watch:  
	ls $(SOURCE) | entr make all
