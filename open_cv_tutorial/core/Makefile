#Compile and link flags
CXX = g++
CFLAGS = -Wall -g
#Compilation
CXXFLAGS += `pkg-config opencv --cflags`

#Linking
LDFLAGS += -lm `pkg-config opencv --libs`

#Name your target executables here
all = DisplayImage SaveImage test Capture scan mask	

all: $(all)

# Program dependencies (.o files will be compiled by implicit rules)
test: 
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ yoo.cpp


DisplayImage: 
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ display_image.cpp

SaveImage: 
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ save_image.cpp

Capture: 
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ capture.cpp

scan: 
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ scan_image.cpp


mask: 
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ mat_mask_operations.cpp

clean:
	rm -f $(all) *.o
