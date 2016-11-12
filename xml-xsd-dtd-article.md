
## Code 1
```xml
<?xml version="1.0"?>
<school>
	<student name="Mario" age="23"/>
	<student name="Romildo" age="21">
		<job position="Software developer">Microsoft</job>
	</student>
</school>
```


## Code 2
```dtd
<!DOCTYPE note
[<!ELEMENT note (to,from,heading,body)>
    <!ELEMENT to (#PCDATA)>
    <!ELEMENT from (#PCDATA)>
    <!ELEMENT heading (#PCDATA)>
    <!ELEMENT body (#PCDATA)>
]>
```

## Code 3
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE note SYSTEM "note.dtd">
<note>
	<to>Tove</to>
	<from>Jani</from>
	<heading>Reminder</heading>
	<body>Don't forget me this weekend!</body>
</note>
```
