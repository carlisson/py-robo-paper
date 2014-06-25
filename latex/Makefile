all :  pdf

pdf :	latex
	dvipdf sbc-template.dvi

latex : sbc-template.tex images
	latex sbc-template.tex
#	makeindex -s main.ist -t main.glg -o main.gls main.glo
	bibtex sbc-template
	latex sbc-template.tex
	latex sbc-template.tex

images: telas tabelas graficos

telas: robotwar.eps pyrobocode.eps

tabelas: avaliacao-conhecimento.eps avaliacao-notas.eps questao1.eps questao2.eps questao3.eps

graficos: g-part.eps g-conhec.eps g-notas.eps g-questao1.eps g-questao2.eps g-questao3.eps

avaliacao-conhecimento.eps: tabelas/avaliacao-conhecimento.png
	convert tabelas/avaliacao-conhecimento.png avaliacao-conhecimento.eps

avaliacao-notas.eps: tabelas/avaliacao-notas.png
	convert tabelas/avaliacao-notas.png avaliacao-notas.eps

questao1.eps: tabelas/questao1.png
	convert tabelas/questao1.png questao1.eps

questao2.eps: tabelas/questao2.png
	convert tabelas/questao2.png questao2.eps

questao3.eps: tabelas/questao3.png
	convert tabelas/questao3.png questao3.eps

g-part.eps: graficos/graf-participacao.png
	convert graficos/graf-participacao.png g-part.eps

g-questao1.eps: graficos/graf-motivacao.png
	convert graficos/graf-motivacao.png g-questao1.eps

g-questao2.eps: graficos/graf-conhecimento-previo.png
	convert graficos/graf-conhecimento-previo.png g-questao2.eps

g-questao3.eps: graficos/graf-jogos.png
	convert graficos/graf-jogos.png g-questao3.eps

g-conhec.eps: graficos/graf-avalicacao-conhecimento.png
	convert graficos/graf-avalicacao-conhecimento.png g-conhec.eps

g-notas.eps: graficos/graf-avalicacao-notas.png
	convert graficos/graf-avalicacao-notas.png g-notas.eps

robotwar.eps: telas/robotwar.png
	convert telas/robotwar.png robotwar.eps

pyrobocode.eps: telas/pyrobocode.png
	convert telas/pyrobocode.png pyrobocode.eps

clean :
	rm *.aux *.bbl *.blg *.dvi *.log *.pdf *.ps *.toc *~ *.lof *.glo *.gls *.ilg *.ist *.glg *.eps
