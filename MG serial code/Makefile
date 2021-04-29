.SUFFIXES:
.SUFFIXES: .o .cpp

#============================================================
TARGET1 = Jacobi_v
TARGET2 = Gauss_v
TARGET3 = Jacobi_w
TARGET4 = Gauss_w

C_SOURCES = Jacobi_v.cpp Gauss_v.cpp Jacobi_w.cpp Gauss_w.cpp
C_OBJS1 = Jacobi_v.o
C_OBJS2 = Gauss_v.o
C_OBJS3 = Jacobi_w.o
C_OBJS4 = Gauss_w.o
MY_INCLUDES = 

CCX = g++
CXXFLAGS =  -std=c++11 -g -O2  $(INC)

#============================================================
all: $(TARGET1)	$(TARGET2) $(TARGET3) $(TARGET4)

.o:.cpp	$(MY_INCLUDES)
	$(CCX)  -c  $(CXXFLAGS) $<  

$(TARGET1) :   $(C_OBJS1)
	$(CCX) $(CXXFLAGS)  $^ $(LIBDIRS)  -o $@

$(TARGET2) :   $(C_OBJS2)
	$(CCX) $(CXXFLAGS)  $^ $(LIBDIRS)  -o $@

$(TARGET3) :   $(C_OBJS3)
	$(CCX) $(CXXFLAGS)  $^ $(LIBDIRS)  -o $@
	
$(TARGET4) :   $(C_OBJS4)
	$(CCX) $(CXXFLAGS)  $^ $(LIBDIRS)  -o $@

# Implicit rules: $@ = target name, $< = first prerequisite name, $^ = name of all prerequisites 
#============================================================

ALL_SOURCES = Makefile $(C_SOURCES) $(MY_INCLUDES)

NOTES =

clean:
	rm -f $(TARGET1) $(C_OBJS1) $(TARGET2) $(C_OBJS2) $(TARGET3) $(C_OBJS3) $(TARGET4) $(C_OBJS4) core  *~


