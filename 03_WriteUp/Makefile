SHELL := /bin/bash

# Retrieves todo items from LaTeX file and prints them (+ their count)
define get_todo_items
	@allTodoItems=$$(grep -i '% todo' Final.tex | wc -l); echo -e "\n\e[33mFound \e[91m$$allTodoItems \e[33mTODO items:\n"
	@grep -i '% todo' Final.tex | while read -r line ; do echo -e "\t \e[92m$$line\n" ; done ; echo -e "\e[39m" 
endef

all:
	pdfcslatex Final.tex
	rm  Final.log Final.aux

todo:
	$(call get_todo_items)