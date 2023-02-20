FILES=copy.md  modes.md  num.md  search.md

all:
	cp editor.md.src editor.md
	for FN in $(FILES); do sed -i -e "/___$${FN}___/r pages/$${FN}" -e "s///"  editor.md ;   done
