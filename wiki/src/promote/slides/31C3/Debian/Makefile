default:	all

%.shtml: %.mdwn reveal.js/LICENSE
	pandoc --self-contained -t revealjs -s $< -o $@

%.mdwn.txt: %.mdwn
	cp -f $< $@

clean:
	rm -f *.shtml *.mdwn.txt

export: Debian.shtml Debian.mdwn.txt

reveal.js/LICENSE:
	git clone https://github.com/hakimel/reveal.js.git reveal.js

all: export
