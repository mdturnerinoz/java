HELLO := hello
JAR   := $(HELLO).jar
SRC   := $(HELLO).java
CLASS := $(HELLO).class
MANF  := $(HELLO).mf
JAVAC := javac
JAVA  := java
all : clean $(JAR) run
$(JAR) : $(CLASS)
	jar vcmf $(MANF) $(JAR) $(CLASS) $(SRC)
	jar tvf  $(JAR)
$(CLASS) : $(SRC)
	$(JAVAC) -cp . $< -d .
run :
	$(JAVA) -jar $(JAR)
clean :
	(rm -fR *.class *.jar *~)
