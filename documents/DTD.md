# Types of DTD Declarations

In a Document Type Definition (DTD), there are four main types of declarations. Each of these helps define different parts of an XML document.

1. **Element Declarations**
2. **Attribute List Declarations**
3. **Entity Declarations**
4. **Notation Declarations**

## 1. Element Declaration

- Element declarations define the structure of elements in XML.
- You use the `<!ELEMENT>` declaration to define an element.

**Syntax:**

```xml
<!ELEMENT element_name content_model >
```

- `element_name`: The name of the element.
- `content_model`: The type of content the element can have. This could be text, another element, or a specific rule.

**Content Models:**

- **ANY**: The element can contain anything (text, elements, or both).
- **EMPTY**: The element cannot contain anything.
- **#PCDATA**: The element can contain only plain text.
- **Element-Only Content**: The element can contain only other elements.
- **Mixed Content**: The element can contain a mix of text and other elements.

### Examples of Element Declarations

#### ANY Content Model

- Allows any content inside the element.

```xml
<!ELEMENT tutorials ANY>
```

#### EMPTY Content Model

- The element is empty (self-closing tag).

```xml
<!ELEMENT header EMPTY>
<header />
```

#### PCDATA (Plain Text) Content Model

- The element can contain plain text.

```xml
<!ELEMENT name (#PCDATA)>
<name>XML Tutorial</name>
```

#### Element-Only Content

- The element must contain one or more specific elements.

```xml
<!ELEMENT tutorials (tutorial)>
<tutorials>
  <tutorial>XML Tutorial</tutorial>
</tutorials>
```

### 2. Element Operators

- Element operators control how many times a child element can appear within an XML document.

#### Zero or More (`*`)

- The child element can appear zero or more times.

```xml
<!ELEMENT tutorials (tutorial*)>
```

#### One or More (`+`)

- The child element must appear at least once.

```xml
<!ELEMENT tutorials (tutorial+)>
```

#### Zero or One (`?`)

- The child element can appear either zero or one time.

```xml
<!ELEMENT tutorials (tutorial?)>
```

#### Choices (`|`)

- Allows choosing between one or more elements.

```xml
<!ELEMENT tutorial (name | title | subject)>
```

### 3. Mixed Content

- Mixed content allows both text and specific elements.

**Syntax:**

```xml
<!ELEMENT element_name (#PCDATA | child_element_name1 | child_element_name2 )*>
```

**Example:**

```xml
<!ELEMENT tutorial (#PCDATA | name | title | subject)*>
```

### 4. DTD Operators with Sequences

- DTD operators with sequences allow more complex structures.

**Syntax:**

```xml
<!ELEMENT element_name (sub_elem1 operator, sub_elem2 operator, ...)>
```

**Example:**

```xml
<!ELEMENT tutorial (name+, url?)>
```

- This means the `tutorial` element contains one or more `name` elements and zero or one `url` element.

### Attribute Declaration

- Attributes give additional information about elements.
- Use `<!ATTLIST>` to declare all attributes for a given element.

**Syntax:**

```xml
<!ATTLIST element_name
  attribute_name attr_type default_value
  ...
>
```

- `element_name`: The element the attributes belong to.
- `attribute_name`: The name of the attribute.
- `attr_type`: The type of value the attribute can have.
- `default_value`: The default value of the attribute.

### Attribute Types

- **CDATA**: Plain text.
- **ID**: A unique identifier.
- **IDREF**: A reference to an ID.
- **NMTOKEN**: A name token (a valid XML name).

**Example:**

```xml
<!ATTLIST tutorial published CDATA "No">
```

### Entity Declaration

- Entities are placeholders for text or data that can be reused throughout the XML document.

**General Entities:**

- Contain XML content.

**Syntax:**

```xml
<!ENTITY name definition>
```

**Example:**

```xml
<!ENTITY author "Homer Flinstone">
```

- You can use this entity in an XML document like this:

```xml
<author>&author;</author>
```

**Parameter Entities:**

- Contain DTD content and can be reused in DTD declarations.

**Syntax:**

```xml
<!ENTITY % name definition>
```

**Example:**

```xml
<!ENTITY % author "<!ELEMENT author EMPTY>">
%author;
```
