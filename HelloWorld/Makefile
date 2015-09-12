# g++ -c -Wall -I /opt/AMDAPP/include/ HelloWorld.cpp
# g++ HelloWorld.o -o host -L /opt/AMDAPP/lib/x86_64/ -l OpenCL

CC=g++

FOLDER_INC= # -I /opt/AMDAPP/include/
FOLDER_LIB= # -L /opt/AMDAPP/lib/x86_64/

CFLAGS=-c -Wall $(FOLDER_INC)
LDFLAGS= $(FOLDER_LIB) -l OpenCL
SOURCES=HelloWorld.cpp
OBJECTS=$(SOURCES:.cpp=.o)
EXECUTABLE=hello

all: $(SOURCES) $(EXECUTABLE)

$(EXECUTABLE): $(OBJECTS) 
	$(CC) $(OBJECTS) -o $@ $(LDFLAGS) 

.cpp.o:
	$(CC) $(CFLAGS) $< -o $@

clean:
	rm -rf *o $(EXECUTABLE)
