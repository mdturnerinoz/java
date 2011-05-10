HELLO := hello
JAR   := $(HELLO).jar
SRC   := $(HELLO).java
CLASS := $(HELLO).class
MANF  := $(HELLO).mf
JAVAC := javac
JAVA  := java
all : $(JAR) runit
$(JAR) : $(CLASS)
	jar cmf $(MANF) $(JAR) $(CLASS) $(SRC)
$(CLASS) : $(SRC)
	$(JAVAC) -cp . $<
runit :
	$(JAVA) -jar $(JAR)
clean :
	(rm -f *.class *~ *.jar)
