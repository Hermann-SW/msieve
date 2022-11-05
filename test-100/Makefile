SHELL := /bin/bash

sed1 = s/^.*202[2-9]  //

all:
	../msieve -S 123456789 987654321 1522605027922533360535618378132637429718068114961380688657908494580122963258952897654000350692006139
	diff msieve.dat*
	diff <(sed "$(sed1)" msieve.log) <(sed "$(sed1)" msieve.log.cmp)

clean:
	rm -f msieve.dat
	rm -f msieve.log

