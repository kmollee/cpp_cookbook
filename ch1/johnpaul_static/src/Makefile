
# Specify extensions of files to delete when cleaning
CLEANEXTS = o a out

OUTPUTFILE = libjohnpaul.a
INSTALLDIR= ../bins

CXXFLAGS = -I../includes
SRCS = john.o paul.o johnpaul.o

all: $(OUTPUTFILE)


# $@ represents the filename of the target,
# $< represents the filename of the first prerequisite
# $^ represents the sequence of prerequisites
# Build libjohnpaul.a from john.o, paul.o, and johnpaul.o
$(OUTPUTFILE): $(SRCS)
	ar rvs $@ $^

install: hello
	mkdir -p $(INSTALLDIR)
	cp -p $(OUTPUTFILE) $(INSTALLDIR)

clean:
	rm -f $(OUTPUTFILE)
	for file in $(CLEANEXTS); do rm -f *.$$file; done

# Indicate dependency of .cpp files on .hpp files
# john.o: john.cc
# paul.o: paul.cc
# johnpaul.o: john.cc paul.cc johnpaul.cc

.PHONY: all install clean