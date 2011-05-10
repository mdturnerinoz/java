HELLO  := hello
SRCDIR := ./src/
BLDDIR := ./build/
DSTDIR := ./dist/
JAR    := $(DSTDIR)$(HELLO).jar
SRC    := $(SRCDIR)$(HELLO).java
CLASS  := $(BLDDIR)$(HELLO).class
MANF   := $(HELLO).mf
JAVAC  := javac
JAVA   := java
all : clean init $(JAR) run
init :
	mkdir ./build
	mkdir ./dist
$(JAR) : $(CLASS)
	jar vcmf $(MANF) $(JAR) $(CLASS)
	jar tvf  $(JAR)
$(CLASS) : $(SRC)
	$(JAVAC) -cp . $< -d .
run :
	$(JAVA) -jar $(JAR) -cp $(BLDDIR)
clean :
	(rm -fR $(BLDDIR) $(DSTDIR) *~ *.jar *.class )

