maak een header met yaml data
header wordt frontmatter genoemd
moet bovenaan staan/moet ermee beginnen
bv:
`---`
titel: property
bla: proertie
tags:
	eerste
	tweede
`---`
als de 3 dashes een streep worden maak er dan even 4 van
dan wordt ie goed geformatteerd.


\`\`\``
dataview
TABLE
	category,
	name,
	score
FROM #music 
\`\`\``


### Basic 
```dataview
TABLE
	category,
	name,
	score
FROM #game 
```
### WHERE
```dataview
TABLE
	category,
	name,
	score
FROM #game 
WHERE score > 5
```
### Sort
```dataview
TABLE
	category,
	name,
	score
FROM #game 
SORT score DESC
```
### Sum
```dataview
TABLE
	category,
	name,
	score,
	sum(score) as totaal
FROM #game 
SORT score DESC
```
### totaal van een column
```dataview
TABLE sum(rows.score) as Totaal  
FROM #game
WHERE score != null 
GROUP BY true
```

Vind Tasks
```dataview
task from "Logboek"
```

Vind Gedane Tasks
```dataview
task from "Logboek" WHERE completed
```

Vind Open Tasks
```dataview
task from "Logboek" WHERE !completed
```


