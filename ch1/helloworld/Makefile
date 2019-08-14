OUTPUTFILE=hello
INSTALLDIR=bin	

all: $(OUTPUTFILE)


# $@ represents the filename of the target,
# $< represents the filename of the first prerequisite
# $^ represents the sequence of prerequisites
$(OUTPUTFILE): main.cc
	g++ -o $@ $<

install: hello
	mkdir -p $(INSTALLDIR)
	cp -p $(OUTPUTFILE) $(INSTALLDIR)

clean:
	rm -f $(OUTPUTFILE)

.PHONY: all install clean