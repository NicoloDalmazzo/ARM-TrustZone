# Main document name (without .tex)
MAIN = report

# Tools
LATEX = pdflatex
BIBER = biber

# Flags
LATEXFLAGS = -interaction=nonstopmode -file-line-error

# Default target
all: $(MAIN).pdf

# Build PDF
$(MAIN).pdf: $(MAIN).tex
	$(LATEX) $(LATEXFLAGS) $(MAIN)
	$(BIBER) $(MAIN)
	$(LATEX) $(LATEXFLAGS) $(MAIN)
	$(LATEX) $(LATEXFLAGS) $(MAIN)

# Clean auxiliary files
clean:
	rm -f \
		*.aux *.bbl *.bcf *.blg *.log *.out *.run.xml \
		*.toc *.lof *.lot *.synctex.gz *.fdb_latexmk *.fls

# Full clean (including PDF)
distclean: clean
	rm -f $(MAIN).pdf

.PHONY: all clean distclean

