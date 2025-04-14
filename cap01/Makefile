# ******************************************************************************
# Variáveis importantes
CC=yasm
CFLAGS=-f elf64 -g dwarf2

LD=ld
LFLAGS=


# ******************************************************************************
# Programas a serem compilados (pode ser tudo em uma única linha, mas colocar um
# nome por linha facilita a exclusão e a visualização):
PROGRAMAS = \
	    exit.o \
	    exit \
	    exercise1.o \
	    exercise1 \
	    exercise2.o \
	    exercise2


# ******************************************************************************
# Regra padrão: compila todos os programas (NÃO ALTERE!)
all: $(PROGRAMAS)


# ******************************************************************************
# Regras individuais de compilação: crie as regras específicas de cada target:
exit.o: exit.asm
	$(CC) $(CFLAGS) -l exit.lst exit.asm

exit: exit.o
	ld -o exit exit.o

exercise1.o: exercise1.asm
	$(CC) $(CFLAGS) -l exercise1.lst exercise1.asm

exercise1: exercise1.o
	ld -o exercise1 exercise1.o

exercise2.o : exercise2.asm
	$(CC) $(CFLAGS) -l exercise2.lst exercise2.asm

exercise2: exercise2.o
	gcc -o exercise2 exercise2.o


# ******************************************************************************
# Regras para a limpeza final (NÃO ALTERE!)
limpar:
	rm -f *~ a.out core graphics.ps

apagar: limpar
	rm -f *.o *.a $(PROGRAMAS)
