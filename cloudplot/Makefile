NODE_PKGS= express

.PHONY: run
run: node-pkgs
	node --jvm --polyglot cloudplot.js

.PHONY: node-pkgs
node-pkgs:
	for i in $(NODE_PKGS) ; do \
    if [ -f node_modules/$${i}/package.json ] ; then continue ; fi ; \
    npm install $${i} ; \
  done
