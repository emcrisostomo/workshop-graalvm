JARFILE= ./target/topten-1.0.jar
SOURCES= TopTen.java

.PHONY: package
package: $(JARFILE)

.PHONY: clean
clean:
	./mvnw clean

.PHONY: run
run: $(JARFIlE)
	java -jar $(JARFILE) *.txt

$(JARFILE): $(SOURCES)
	./mvnw package
