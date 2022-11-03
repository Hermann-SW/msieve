SHELL := /bin/bash

sed1 = s/^.*2022  //

all:
	../msieve -S 123456789 987654321 71641520761751435455133616475667090434063332228247871795429
	diff msieve.dat*
	diff <(sed "$(sed1)" msieve.log) <(sed "$(sed1)" msieve.log.cmp)

clean:
	rm -f msieve.dat
	rm -f msieve.log

