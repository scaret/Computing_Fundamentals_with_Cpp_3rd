src = $(shell find ./ -name "*.md")
docx = $(src:%.md=../docx/%.docx)

all: $(docx) $(pdf)

../docx/%.docx:%.md
	pandoc -f markdown+tex_math_dollars -t docx $< -o $@  --latex-engine=xelatex

clean:
	rm -rf $(docx)