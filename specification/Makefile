HEADER_SOURCE := header.adoc
PDF_RESULT ?= riscv-cove.pdf

all: build

build:

	@echo "Building asciidoc"
	asciidoctor-pdf \
    --trace \
    --attribute=allow-uri-read \
    --attribute=mathematical-format=svg \
    --attribute=pdf-fontsdir=docs-resources/fonts \
    --attribute=pdf-style=docs-resources/themes/riscv-pdf.yml \
    --failure-level=ERROR \
    --require=asciidoctor-bibtex \
    --require=asciidoctor-diagram \
    --require=asciidoctor-mathematical \
    --require=asciidoctor-kroki \
    --out-file=$(PDF_RESULT) \
    $(HEADER_SOURCE)

clean:
	rm $(PDF_RESULT)
