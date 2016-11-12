# DTD and XSD - The XML side you didn’t now about


## document1.xml
```xml
<?xml version="1.0"?>
<school>
	<student name="Mario" age="23"/>
	<student name="Romildo" age="21">
		<job position="Software developer">Microsoft</job>
	</student>
</school>
```


## document2.dtd
from http://www.w3schools.com/xml/xml_dtd_intro.asp
```dtd
<!DOCTYPE note
[<!ELEMENT note (to,from,heading,body)>
    <!ELEMENT to (#PCDATA)>
    <!ELEMENT from (#PCDATA)>
    <!ELEMENT heading (#PCDATA)>
    <!ELEMENT body (#PCDATA)>
]>
```

## document3.xml
from http://www.w3schools.com/xml/xml_dtd_intro.asp
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

## document4.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE note SYSTEM "note.dtd">
<note>
	<to>Tove</to>
	<origin>Jani</origin>
	<heading>Reminder</heading>
	<body>Don't forget me this weekend!</body>
	<sender>Mario</sender>
</note>
```


## document5.xsd
```xsd
<?xml version="1.0" encoding="UTF-8"?>
<schema xmlns="http://www.w3.org/2001/XMLSchema" 
	targetNamespace="http://yournamespane.comesHere.com/whateve">
	<!--Elements and restrictions come here-->
</schema>
```


## document6.xsd
```xsd
<?xml version="1.0" encoding="UTF-8"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
	targetNamespace="http://yournamespane.comesHere.com/whatever">
	<!--Elements and restrictions come here-->
</xsd:schema>
```

## document7.xsd
```xsd
<?xml version="1.0" encoding="UTF-8"?>
<schema xmlns="http://www.w3.org/2001/XMLSchema" 
		targetNamespace="http://example1.xsd"
		xmlns:example="http://example1.xsd" elementFormDefault="qualified">

	<complexType name="PersonType">
		<all>
			<element name="full-name" type="string" minOccurs="1" maxOccurs="1"/>
			<element name="age" type="integer" minOccurs="1" maxOccurs="1"/>
		</all>
	</complexType>

	<element name="Person" type="example:PersonType" nillable="false"/>

</schema>
```

## document8.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<Person xmlns="http://example1.xsd">
	<age>23</age>
	<full-name>MarioJ.F.Junior</full-name>
</Person>
```

