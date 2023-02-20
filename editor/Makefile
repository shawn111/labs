FILES=$(shell ls pages)
HFILES=$(shell ls ../helix)


renew:
	cp pages/editor-src.md editor.md
	for FN in $(FILES); do sed -i -e "/___$${FN}___/r pages/$${FN}" -e "s///" editor.md; done
	for FN in $(HFILES); do sed -i -e "/===$${FN}===/r ../helix/$${FN}" -e "s///" editor.md; done
	
html: renew
	echo y | npx @marp-team/marp-cli@latest editor.md

pdf: renew
	echo y | npx @marp-team/marp-cli@latest --pdf editor.md

all: pdf html
