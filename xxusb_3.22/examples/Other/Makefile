# basic makefile

.LIBPATTERNS ="'lib%.so lib%.a' "

CXX   = g++
FC		= g77
F90		= f90
RM		= rm -f
CC		= g++

LD            = g++
LDFLAGS       = -O
SOFLAGS       = -shared


CXXLIBDIRS	= -L./../../libs/
CXXLIBS		= -lxx_usb -lm
INCLUDEDIRS 	= -I./../../include/

CXXFLAGS      	= -O -Wall -fPIC -g $(INCLUDEDIRS)

CFLAGS		+= $(INCLUDEDIRS) $(SOFLAG)
CFLAGS		+= $(CXXLIBDIRS) $(CXXLIBS)
LDFLAGS		= $(CXXFLAGS)

OBJ = ./IRQ

main: 
	$(CXX) $(CXXFLAGS) \
	$(CXXLIBS) $(CXXLIBDIRS) -o $(OBJ) VDIS_IRQ_test_001.cpp
	@echo "Done"



clean:
	$(RM) $(OBJ) 

