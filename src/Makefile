# Build the public class edition of "Notes in Modern Analysis" (MATH S4061).
# Requires TeX Live or MacTeX (pdflatex + makeindex).
TEX = pdflatex -interaction=nonstopmode
LECTURES = chapter-00 lecture-01 lecture-02 lecture-03 lecture-04 lecture-05 lecture-06 lecture-07

.PHONY: all book lectures clean

# Complete notes (class edition) + every lecture as a standalone PDF.
all: book lectures

# The complete notes -> main-class.pdf
book:
	$(TEX) main-class.tex
	makeindex main-class.idx
	$(TEX) main-class.tex
	$(TEX) main-class.tex

# Each lecture / chapter-00 as its own PDF.
lectures:
	@for u in $(LECTURES); do \
		$(TEX) $$u.tex; \
		$(TEX) $$u.tex; \
	done

clean:
	rm -f *.aux *.log *.out *.toc *.loo *.idx *.ind *.ilg *.fls *.fdb_latexmk *.synctex.gz
	rm -f main-class*.pdf chapter-00.pdf lecture-*.pdf exercises-*.pdf
