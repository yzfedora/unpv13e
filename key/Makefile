include ../Make.defines

PROGS =	dump register add
OBJS = printsadbmsg.o name.o

all: ${PROGS}

dump: ${OBJS} dump.o
	${CC} ${CFLAGS} -o $@ $@.o ${OBJS} ${LIBS}

register: register.o ${OBJS}
	${CC} ${CFLAGS} -o $@ $@.o ${OBJS} ${LIBS}

add: add.o ${OBJS}
	${CC} ${CFLAGS} -o $@ $@.o ${OBJS} ${LIBS}

%.o: %.c unp.h
	$(CC) $(CFLAGS) -c $^ $(LIBS)

clean:
	$(RM) $(OBJS) $(PROGS) $(wildcard *.o) $(wildcard *.h.gch)
