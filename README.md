# A SIMPLE JQ TEST #

You want to work with jq and get some results, that obvious, but is `jq` allready installed on your system?
Lets find out...

## STEPS ##

* Open `Terminal`
* type in `which jq` or `jq --version`
	* this should give you an answer if `jq` is installed.

### jq is not installed (oops...) ###

#### MAC ####

If `jq` isn't installed on your MAC you have several options;

* install with homebrew; `brew install jq`
	* if you don't have homebrew installed follow the steps on http://brew.sh
* install from the jq homepage http://stedolan.github.io/jq/download/

#### PC ####

If `jq` isn't installed on your Windos Thingy you have to install from the jq homepage http://stedolan.github.io/jq/download/

## Test and play with `jq` ##

* if `jq` is installed:
	* place the directory named `jq-test` in a convienent location on your hard-drive
	* in `Terminal` change directory with `cd /path/to/jq-test`
	* type `pwd` to check the present working directory (`pwd`)
	* type `cat jason-jq-test.txt | jq '.name'`
	* the return value in Terminal should be: `UvA`
	* now try: `cat jason-jq-test.txt | jq '.faculties'`
	* the return values in Terminal should be:
												```
												[
												  {
												    "name": "Faculteit Economie en Bedrijfskunde"
												  },
												  {
												    "name": "Faculteit der Geesteswetenschappen"
												  },
												  {
												    "name": "Faculteit der Geneeskunde"
												  },
												  {
												    "name": "Faculteit der Natuurwetenschappen, Wiskunde en Informatica"
												  },
												  {
												    "name": "Faculteit der Maatschappij- en Gedragswetenschappen"
												  },
												  {
												    "name": "Faculteit der Rechtsgeleerdheid"
												  },
												  {
												    "name": "Faculteit der Tandheelkunde"
												  }
												]	
												```

* navigating down the `JSON` tree;
	* type `cat jason-jq-test.txt | jq '.location.street'`
	* the return value in Terminal should be: `Spui 21`
* At least now you know if `jq` is installed and working

### `jq` Manual ###

To learn all the `jq` commands and options visit: 

http://stedolan.github.io/jq/manual/

Happy `jq`ing...

### Feedback ###

If you have questions or want to give some feedback you can contact me @ objects2data@gmail.com