# basic makefile
here=$(shell pwd)

.LIBPATTERNS ="'lib%.so lib%.a' "

CXX   = gcc
FC		= g77
F90		= f90
RM		= rm -f
CC		= g++

LD            = gcc
LDFLAGS       = -O
SOFLAGS       = -shared


CXXLIBDIRS	= -L./../../lib/
CXXLIBS		= -lxx_usb -lm -lusb -Wl,"-rpath=$(here)/../../lib"
INCLUDEDIRS 	= -I./../../include/

CXXFLAGS      	= -O -Wall -fPIC -g $(INCLUDEDIRS)

CFLAGS		+= $(INCLUDEDIRS) $(SOFLAG)
CFLAGS		+= $(CXXLIBDIRS) $(CXXLIBS)
LDFLAGS		= $(CXXFLAGS)

OBJ = ./vmereset

main: 
	$(CXX) $(CXXFLAGS) VM-USB_reset.c \
	$(CXXLIBS) $(CXXLIBDIRS) -o $(OBJ) 
	@echo "Done"



clean:
	$(RM) $(OBJ) 


