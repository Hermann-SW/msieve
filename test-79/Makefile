SHELL := /bin/bash

sed1 = s/^.*2022  //

all:
	../msieve -S 123456789 987654321 7293469445285646172092483905177589838606665884410340391954917800303813280275279
	diff msieve.dat*
	diff <(sed "$(sed1)" msieve.log) <(sed "$(sed1)" msieve.log.cmp)

clean:
	rm -f msieve.dat
	rm -f msieve.log

