JARFILE= ./target/benchmarks.jar
SOURCES= src/main/java/valhallaBench/Multiply.java \
         src/main/java/valhallaBench/Complex.java

.PHONY: package
package: $(JARFILE)

.PHONY: clean
clean:
	./mvnw clean

.PHONY: run
run: $(JARFILE)
	java -jar $(JARFILE)

$(JARFILE): $(SOURCES)
	./mvnw package
