#!/usr/bin/make -f

SRC_DIR ?= .

DEST_LAUNCHER = libopenh264-launch

build: $(DEST_LAUNCHER)

clean:
	rm -f $(DEST_LAUNCHER)

$(DEST_LAUNCHER):
	@echo "#!/bin/bash" > $(DEST_LAUNCHER)
	@cat $(SRC_DIR)/init >> $(DEST_LAUNCHER)
	@cat $(SRC_DIR)/library-exports >> $(DEST_LAUNCHER)
	@cat $(SRC_DIR)/mark-and-exec >> $(DEST_LAUNCHER)

install: $(DEST_LAUNCHER)
	install -D -m755 $(DEST_LAUNCHER) $(DESTDIR)/bin/$(DEST_LAUNCHER)
