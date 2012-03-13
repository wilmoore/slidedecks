SHELL		=	/bin/bash

notes:	README.html
	cat README.html | htmldoc --footer . -f diy-private-cloud-notes.pdf -

README.html:
	pandoc -f markdown -o README.html README.md

clean:
	rm README.html diy-private-cloud-notes.pdf
