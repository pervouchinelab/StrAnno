.PHONY : all

all :: hg19/trackDB.txt hg38/trackDB.txt

hg19/trackDB.txt : ../human/hg19/rin/trackDB.txt
	for f in `ls ../human/hg19/rin/*.bed`; do echo $$f; g=$$(basename $$f); sort -k1,1 -k2,2n $$f > hg19/$$g; ../bedToBigBed hg19/$$g hg19/hg19.chrom.sizes hg19/$${g%.*}.bb; done
	cp ../human/hg19/rin/trackDB.txt hg19/


hg38/trackDB.txt : ../human/hg38/rin/trackDB.txt
	for f in `ls ../human/hg38/rin/*.bed`; do echo $$f; g=$$(basename $$f); sort -k1,1 -k2,2n $$f > hg38/$$g; ../bedToBigBed hg38/$$g hg38/hg38.chrom.sizes hg38/$${g%.*}.bb; done
	cp ../human/hg38/rin/trackDB.txt hg38/

