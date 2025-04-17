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
	    float.o \
	    integer.o


# ******************************************************************************
# Regra padrão: compila todos os programas (NÃO ALTERE!)
all: $(PROGRAMAS)


# ******************************************************************************
# Regras individuais de compilação: crie as regras específicas de cada target:
float.o: float.asm
	$(CC) $(CFLAGS) -l float.lst float.asm

integer.o: integer.asm
	$(CC) $(CFLAGS) -l integer.lst integer.asm


# ******************************************************************************
# Regras para a limpeza final (NÃO ALTERE!)
limpar:
	rm -f *~ a.out core graphics.ps

apagar: limpar
	rm -f *.o *.a *.lst $(PROGRAMAS)
