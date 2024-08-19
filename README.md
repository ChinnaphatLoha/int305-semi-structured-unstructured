# INT305 - Semi-Structured and Unstructured Data Management

## What Is Semi-Structured Data?

Semi-structured data is a type of data that doesn't fit into traditional tables (like in a database) but still has some organization. Think of it as a mix between structured data (which is very organized) and unstructured data (like plain text). It might have tags or markers to help identify different parts, but it doesn't follow a strict set of rules. Examples include JSON, XML, and HTML.

## Main Language Elements of XML

XML (eXtensible Markup Language) is a way to store and share data in a format that's easy for both humans and computers to read. Here are the main parts of XML:

- **Elements:** The basic building blocks of XML. They have a start tag (`<tagname>`) and an end tag (`</tagname>`), with the content in between.

- **Attributes:** Extra information about elements, written inside the start tag. For example: `<person age="30">John Doe</person>`.

- **Prolog:** The beginning part of an XML file, which tells the computer what version of XML is being used. For example: `<?xml version="1.0" encoding="UTF-8"?>`.

- **Comments:** Notes you can add that are ignored by the computer. They look like this: `<!-- This is a comment -->`.

- **CDATA Sections:** These are used when you want to include text that shouldn't be treated as XML code. It's wrapped like this: `<![CDATA[ Some text ]]>`.

- **Namespaces:** Used to avoid naming conflicts in XML by giving elements a unique prefix. For example: `<prefix:element xmlns:prefix="URI">Content</prefix:element>`.

## Well-Formed vs. Valid XML

- **Well-Formed XML:** A well-formed XML document follows the basic rules of XML:

  - Every tag is opened and closed properly.
  - Tags are nested correctly (no overlapping).
  - There is one root element that wraps everything.
  - Attribute values are surrounded by quotes.

  A well-formed XML document can be read by any XML parser, but it doesn't have to follow a specific structure or set of rules.

- **Valid XML:** A valid XML document is well-formed and follows a specific set of rules (like a recipe). These rules are defined by a Document Type Definition (DTD) or an XML Schema. Valid XML ensures that the structure and content are exactly what they should be, making the document reliable for certain tasks.

## How Document Type Definitions (DTDs) Define XML Syntax

A Document Type Definition (DTD) is like a blueprint that describes the structure of an XML document. It tells you what elements, attributes, and order are allowed in the XML file. There are two types of DTDs:

- **Internal DTD:** Written inside the XML document itself. It looks like this:

```xml
  <!DOCTYPE note [
    <!ELEMENT note (to,from,heading,body)>
    <!ELEMENT to (#PCDATA)>
    <!ELEMENT from (#PCDATA)>
    <!ELEMENT heading (#PCDATA)>
    <!ELEMENT body (#PCDATA)>
  ]>
  <note>
    <to>Tove</to>
    <from>Jani</from>
    <heading>Reminder</heading>
    <body>Don't forget me this weekend!</body>
  </note>
```

In this example, the DTD defines that a `note` element must include `to`, `from`, `heading`, and `body` elements, and each of these elements contains text.

- **External DTD:** Stored outside the XML document and linked to it. It might look like this:

```xml
  <!DOCTYPE note SYSTEM "note.dtd">
  <note>
    <to>Tove</to>
    <from>Jani</from>
    <heading>Reminder</heading>
    <body>Don't forget me this weekend!</body>
  </note>
```

  Here, the DTD is saved in a separate file called `note.dtd`, and the XML document refers to it.

Using a DTD ensures that your XML document is valid and follows the correct structure, making it easier to share and use the data with confidence.
