SOURCES=      Distance.java
MAIN_CLASS=   Distance.class
NATIVE_IMAGE= ./distance

.PHONY: install-native-image
install-native-image:
	gu install native-image

.PHONY: clean
clean:
	-rm $(MAIN_CLASS)
	-rm $(NATIVE_IMAGE)

.PHONY: run
run: $(MAIN_CLASS)
	java -cp sis.jar:. Distance 1 2 3 4

.PHONY: run-native
run-native: $(NATIVE_IMAGE)
	$(NATIVE_IMAGE) 1 2 3 4

$(MAIN_CLASS):
	javac -cp sis.jar $(SOURCES)

.PHONY: native
native: $(NATIVE_IMAGE)

$(NATIVE_IMAGE): $(MAIN_CLASS)
	native-image -cp sis.jar:. Distance
