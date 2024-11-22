SUBDIRS = src
dist_doc_DATA = README
AM_CFLAGS = -std=c17 -Ofast -march=native -Werror -Wall -Wextra -Wpedantic \
	  -Wshadow -Wconversion -pedantic-errors -Wstrict-prototypes \
	  -Wold-style-definition -O3 -g

size:
	wc --bytes src/char80

clean-local: format-c format-h remove-orig remove-executable

format-c:
	astyle --quiet --recursive --style=gnu --indent=force-tab=8 \
		--delete-empty-lines --max-code-length=79 --lineend=linux \
		--indent-preproc-block --indent-col1-comments --indent-cases \
		"*.c"

format-h:
	astyle --quiet --recursive --style=gnu --indent=force-tab=8 \
		--delete-empty-lines --max-code-length=79 --lineend=linux \
		--indent-preproc-block --indent-col1-comments --indent-cases \
		"*.h"
remove-orig:
	find . -name '*.orig' -exec rm -f {} +

remove-executable:
	rm src/char80

hexdump:
	hexdump -C src/char80 | less

disasm:
	objdump -d src/char80
