#/bin/bash -ex

AMUN=../../../amun/build/amun
DIFF=../../scripts/diff.py -p 0.002

test:
	cat test.in |  $(AMUN) -c config.yml --n-best yes --mini-batch 8 --maxi-batch 32 > test.out
	$(DIFF) test.out test.correct > test.diff

clean:
	rm -f test.out test.diff err
