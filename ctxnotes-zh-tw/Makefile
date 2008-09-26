PRODUCT=ctxnotes
READER=evince

all:
	context --mode=screen $(PRODUCT)
	context --purge

print:
	context --mode=print $(PRODUCT)
	context --purge

bibs:
	context --mode=screen --once $(PRODUCT) \
        && bibtex $(PRODUCT) \
        && context --mode=screen $(PRODUCT)

bibp:
	context --mode=print --once $(PRODUCT) \
        && bibtex $(PRODUCT) \
        && context --mode=print $(PRODUCT)

pdf:
	$(READER) $(PRODUCT).pdf &

clean:
	context --purge
	rm -f *.aux *.bbl *.blg
	rm -f *.pdf
