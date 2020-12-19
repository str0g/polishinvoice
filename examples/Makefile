all: clean fvat.pdf

pdf: fvat.pdf fvat_different_address.pdf fvat_embedded_image

fvat.pdf: fvat.tex
	pdflatex $^

fvat_different_address.pdf: fvat_different_address.tex
	pdflatex $^

fvat_embedded_image.pdf: fvat_embedded_image.tex
	pdflatex --shell-escape $^

clean:
	rm -f *.ps *.dvi *.aux *.toc *.idx *.ind *.ilg *.log *.out *.pdf *.64 fvat_embedded_image.png
