FILES=copy.md  modes.md  num.md  search.md

renew:
	cp editor-src.md editor.md
	for FN in $(FILES); do sed -i -e "/___$${FN}___/r pages/$${FN}" -e "s///" editor.md; done
	
html: renew
	npx @marp-team/marp-cli@latest editor.md

pdf: renew
	npx @marp-team/marp-cli@latest --pdf editor.md

all: pdf html
