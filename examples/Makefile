all: clean fvat.pdf

pdf: fvat.pdf fvat_different_address.pdf

fvat.pdf: fvat.tex
	pdflatex $^
	makeindex fvat.idx
	pdflatex $^
	latex_count=5 ; \
	while egrep -s 'Rerun (LaTeX|to get cross-references right)' fvat.log && [ $$latex_count -gt 0 ] ;\
	    do \
	      echo "Rerunning latex...." ;\
	      pdflatex $^ ;\
	      latex_count=`expr $$latex_count - 1` ;\
	    done

fvat_different_address.pdf: fvat_different_address.tex
	pdflatex $^
	makeindex fvat_different_address.idx
	pdflatex $^
	latex_count=5 ; \
	while egrep -s 'Rerun (LaTeX|to get cross-references right)' fvat_different_address.log && [ $$latex_count -gt 0 ] ;\
	    do \
	      echo "Rerunning latex...." ;\
	      pdflatex $^ ;\
	      latex_count=`expr $$latex_count - 1` ;\
	    done

clean:
	rm -f *.ps *.dvi *.aux *.toc *.idx *.ind *.ilg *.log *.out fvat.pdf fvat_different_address.pdf
