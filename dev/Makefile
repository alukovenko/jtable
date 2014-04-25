
JS=jquery.jtable.header.txt jquery.jtable.core.js jquery.jtable.utils.js jquery.jtable.forms.js jquery.jtable.creation.js  jquery.jtable.editing.js jquery.jtable.deletion.js jquery.jtable.selecting.js jquery.jtable.paging.js jquery.jtable.sorting.js jquery.jtable.dynamiccolumns.js jquery.jtable.masterchild.js

LIB=../lib/
JSOUT=$(LIB)jquery.jtable.js
JSMIN=$(LIB)jquery.jtable.min.js
UGLIFY=uglifyjs
UGLIFYOPTS=--compress --mangle --comments --screw-ie8 --comments '/Copyright/'

all: js uglify

clean:
	\rm -f $(JSOUT) $(JSMIN)

js:
	cat $(JS) | sed 's/^\xEF\xBB\xBF/\r\n/' > $(JSOUT)

uglify:
	$(UGLIFY) $(JSOUT) $(UGLIFYOPTS) --output $(JSMIN)

