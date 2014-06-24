all :  pdf

pdf :	latex
	dvipdf sbc-template.dvi

latex : sbc-template.tex images
	latex sbc-template.tex
#	makeindex -s main.ist -t main.glg -o main.gls main.glo
	bibtex sbc-template
	latex sbc-template.tex
	latex sbc-template.tex

images: fig1.eps fig2.eps table.eps

fig1.eps: fig1.jpg
	convert fig1.jpg fig1.eps

fig2.eps: fig2.jpg
	convert fig2.jpg fig2.eps

table.eps: table.jpg
	convert table.jpg table.eps

clean :
	rm *.aux *.bbl *.blg *.dvi *.log *.pdf *.ps *.toc *~ *.lof *.glo *.gls *.ilg *.ist *.glg
