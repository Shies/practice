calc:calc.y calc.l
	flex -o calc.lex.c calc.l
	bison -d calc.y
	gcc -o $@ calc.tab.c calc.lex.c -lfl 

#calc.lex: calc.y calc.l
#	bison -d calc.y 
#	flex -o calc.lex.c calc.l 
#	g++ -D CALC_LEX -o $@ calc.lex.c -lfl 
clean:
	rm -f calc.lex.c
	rm -f calc.tab.h
	rm -f calc.tab.c
	rm -f calc
test:
	./calc < testdata
run:
	./calc
