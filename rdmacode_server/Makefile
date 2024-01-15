.PHONY: all clean

CC := gcc
CFLAGS := -Wall -g
LDLIBS := -lrdmacm -libverbs -lpthread -g

SRCS := $(wildcard *.c)
APPS := $(SRCS:.c=)

all: $(APPS)

%: %.c
	$(CC) $(CFLAGS) $< -o $@ $(LDLIBS)

clean:
	rm -f $(APPS)