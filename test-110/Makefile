SHELL := /bin/bash

sed1 = s/^.*202[2-9]  //

all:

	if [[ ! -f msieve.dat.cmp ]]; then wget https://stamm-wilbrandt.de/msieve/test-110/msieve.dat.cmp; fi
	../msieve -S 123456789 987654321 35794234179725868774991807832568455403003778024228226193532908190484670252364677411513516111204504060317568667
	diff msieve.dat*
	diff <(sed "$(sed1)" msieve.log) <(sed "$(sed1)" msieve.log.cmp)

clean:
	rm -f msieve.dat
	rm -f msieve.log

