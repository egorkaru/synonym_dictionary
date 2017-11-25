# "Russians synonym dictionary" by N. Abramov

This is a JSON representation of "Russians synonym dictionary" by N. Abramov. It was parsed from text file, then merged with hyphenation dictionary from "Dictionaries for Russian" by OpenOffice.org.

## Raw data sources

* "Russians synonym dictionary" by N. Abramov can be found as text in human readble format [here](http://speakrus.ru/dict/#abramov)
* "Dictionaries for Russian" by OpenOffice.org can be found [here](https://extensions.openoffice.org/en/project/slovari-dlya-russkogo-yazyka-dictionaries-russian)

## Contents

* ```dictionary.json```: The whole dictionary as JSON file; Data still is pretty raw. Words can repeat, some records needs to be unioned, or deleted as unnecessary. Key "wordlist" contains all word in array, sorted alphabetically, i.e. ```{ "wordlist": [...19430 words] }```

Word example:

```
{ 
		"id": 48,
		"name": "Ад",
		"definition": "(кромешный), геенна (огненная), кромешная, преисподняя, бездна, пекло, чистилище, тартар, царство теней (Плутона). Прот. <Рай>. Ср. <Беспорядок>. См. беспорядок || кромешный ад",
		"synonyms": [
				"геенна",
				"кромешная",
				"преисподняя",
				"бездна",
				"пекло",
				"чистилище",
				"тартар",
				"царство теней"
		],
		"antonyms": [
				"рай"
		],
		"similars": [
				"беспорядок"
		]
}
```

* ```schema/dictionary.json```: contain dictionary JSON Schema. 
* ```schema/word.json```: contain word JSON Schema. 
* ```raw/dict1w.txt```: Abramov`s dictionary as plain text file. Was converted to UTF-8.
* ```raw/th_ru_RU_v2.dat```: Hyphenation dictionary as addition source of data

## Scripts

All scripts were written in JS. After nights without sleep. Some parts of work was made in Node.js REPL and now missing. All scripts will be available after implementation missing parts and refactoring existing code.

## Usage

 ```dictionary.json``` is just a JSON file. 
 
 ```javascript
 
 const Dictionary = require('./dictionary.json')
 console.log(Dictionary.wordlist) // Wow 19430 Russian words at the fingertips

 ```
 
 I have no ideas how you will use it. Use it at your discretion. 

## License

```dictionary.json``` available under the terms of the MIT License.

Hyphenation dictionary from "Dictionaries for Russian" by OpenOffice.org licensed under GNU LGPL, conversion author is Peter Novodvorsky.

Сonversion of "Russians synonym dictionary" by N. Abramov was done by Aleksandr Ilin in 2003.