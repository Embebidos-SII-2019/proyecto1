OPO=gpio.o servidor.o main.o 
LIB=../lib
INCLUDE=../include
FLAG1=-Wall -c 
FLAG2=-Wall -o 

output.o: $(OPO)
		$(CC) $(OPO) $(FLAG2) ../bin/output -lpthread

servidor.o: $(LIB)/servidor.c $(INCLUDE)/servidor.h
		$(CC) $(FLAG1) ../lib/servidor.c

gpio.o: $(LIB)/gpio.c $(INCLUDE)/gpio.h
		$(CC) $(FLAG1) ../lib/gpio.c

main.o: main.c
		$(CC) $(FLAG1) main.c 