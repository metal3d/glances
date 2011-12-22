all: bin

cython:
	cython --embed ../glances.py -o glances.c

bin: cython
	gcc glances.c -o glances $$(pkg-config python --cflags --libs)

install:
	install -m666 glances /usr/local/bin
