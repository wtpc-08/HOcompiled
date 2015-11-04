.PHONY: default help preprocessing assembler object executable all clean
CC = gcc
SOURCE = calculator.c
OBJECTS = calculator.o
default: help

help: 	
	@echo "\
Options:\n\n\
  make preprocessing: gcc runs up to pre-processor and stops, creating calculator.pp.c\n\
  make assembler:     gcc runs up to assembler code generation and stops, creating calculator.asm\n\
  make object:        gcc runs up to the creation of the binary object calculator.o\n\
  make executable:    gcc goes all the way and creates the executable calculator.e\n\
  make all:           build all previous\n\
  make clean:         delete output files"

preprocessing: calculator.pp.c

assembler: calculator.asm

object: calculator.o

executable: calculator.e

all: preprocessing assembler object executable

%.pp.c: %.c
	$(CC) -E $^ -o $@ 

%.asm: %.c
	$(CC) -masm=intel -S $^ -o $@ 

%.o: %.c
	$(CC) -c $^ -o $@

%.e: $(OBJECTS)
	$(CC) $^ -o $@

clean:
	rm -rf *.pp.c *.asm *.o *.e
