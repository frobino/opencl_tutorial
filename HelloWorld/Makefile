# g++ -c -Wall -I /opt/AMDAPP/include/ HelloWorld.cpp
# g++ HelloWorld.o -o host -L /opt/AMDAPP/lib/x86_64/ -l OpenCL

CC=g++

FOLDER_INC=/opt/AMDAPP/include/
FOLDER_LIB=/opt/AMDAPP/lib/x86_64/

CFLAGS=-c -Wall -I $(FOLDER_INC)
LDFLAGS= -L $(FOLDER_LIB) -l OpenCL
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
