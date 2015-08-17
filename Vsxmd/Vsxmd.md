# Vsxmd

## AssemblyUnit

##### Namespace

Vsxmd.Units

##### Summary

Assembly unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `AssemblyUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The assembly XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `assembly`. |

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

## BaseUnit

##### Namespace

Vsxmd.Units

##### Summary

The base unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `BaseUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The XML element. |
| elementName | System.String | The expected XML element name. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML `element` name not matches the expected `elementName`. |

### Element `property`

##### Summary

Gets the XML element.

##### Parameters

This method has no parameters.

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

## Converter

##### Namespace

Vsxmd

##### Summary

Convert from XML docuement to Markdown syntax.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `Converter` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| xmlPath | System.String | The XML document path. |

### ToMarkdown `method`

##### Summary

Convert to Markdown syntax.

##### Returns

The generated Markdown content.

##### Parameters

This method has no parameters.

## ExampleUnit

##### Namespace

Vsxmd.Units

##### Summary

Example unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ExampleUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The example XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `example`. |

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the example XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The example XML element. |

## ExceptionUnit

##### Namespace

Vsxmd.Units

##### Summary

Exception unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ExceptionUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The exception XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `exception`. |

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the exception XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The exception XML element list. |

## Extensions

##### Namespace

Vsxmd.Units

##### Summary

Extensions helper.

### Escape `method`

##### Summary

Escape the content to keep it raw in Markdown syntax.

##### Returns

The escaped content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| content | System.String | The content. |

### Join `method`

##### Summary

Concatenates the `value`s with the `separator`.

##### Returns

The concatenated string.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| value | System.Collections.Generic.IEnumerable{System.String} | The string values. |
| separator | System.String | The separator. |

### NthLastOrDefault\`\`1 `method`

##### Summary

Gets the n-th last element from the `source`.

##### Returns

The target element, default(`TSource`) if not found.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| source | System.Collections.Generic.IEnumerable{``0} | The source enumerable. |
| index | System.Int32 | The index for the n-th last. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| TSource | The type of the elements of `source`. |

### TakeAllButLast\`\`1 `method`

##### Summary

Take all element except the last `count`.

##### Returns

The generated enumerable.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| source | System.Collections.Generic.IEnumerable{``0} | The source enumerable. |
| count | System.Int32 | The number to except. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| TSource | The type of the elements of `source`. |

### ToMarkdownText `method`

##### Summary

Convert the inline XML nodes to Markdown text. For example, it works for `summary` and `returns` elements.

##### Returns

The generated Markdwon content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The XML element. |

##### Example

This method converts the following `summary` element

```
<summary>The <paramref name="element" /> value is <value>null</value>, it throws <c>ArgumentException</c>. For more, see <see cref="M:Vsxmd.Units.Extensions.ToMarkdownText(System.Xml.Linq.XElement)" />.</summary>
```

To the below Markdown content.

```
The `element` value is `null`, it throws `ArgumentException`. For more, see `ToMarkdownText`.
```

## IUnit

##### Namespace

Vsxmd.Units

##### Summary

`IUnit` is wrapper to handle XML elements.

### ToMarkdown `method`

##### Summary

Represent the XML element content as Markdown syntax.

##### Returns

The generated Markdown content.

##### Parameters

This method has no parameters.

## MemberKind

##### Namespace

Vsxmd.Units

##### Summary

The member kind.

### Constants `constants`

##### Summary

Constants

##### Parameters

This method has no parameters.

### Constructor `constants`

##### Summary

Constructor.

##### Parameters

This method has no parameters.

### Method `constants`

##### Summary

Method.

##### Parameters

This method has no parameters.

### NotSupported `constants`

##### Summary

Not supported member kind.

##### Parameters

This method has no parameters.

### Property `constants`

##### Summary

Property.

##### Parameters

This method has no parameters.

### Type `constants`

##### Summary

Type.

##### Parameters

This method has no parameters.

## MemberUnit

##### Namespace

Vsxmd.Units

##### Summary

Member unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `MemberUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The member XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `member`. |

### Comparer `property`

##### Summary

Gets the member unit comparer.

##### Parameters

This method has no parameters.

### Kind `property`

##### Summary

Gets the member kind, one of `MemberKind`.

##### Parameters

This method has no parameters.

### Name `property`

##### Summary

Gets the name.

##### Parameters

This method has no parameters.

##### Example

`Vsxmd.Units.TypeUnit`, `Vsxmd.Units.TypeUnit.#ctor(System.Xml.Linq.XElement)`, `Vsxmd.Units.TypeUnit.TypeName`.

### NamespaceName `property`

##### Summary

Gets the namespace name.

##### Parameters

This method has no parameters.

##### Example

`Vsxmd`, `Vsxmd.Units`.

### TypeFullName `property`

##### Summary

Gets the type full name.

##### Parameters

This method has no parameters.

##### Example

`Vsxmd.Program`, `Vsxmd.Units.TypeUnit`.

### TypeName `property`

##### Summary

Gets the type name.

##### Parameters

This method has no parameters.

##### Example

`Program`, `Converter`.

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

### Compare `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

## ParamUnit

##### Namespace

Vsxmd.Units

##### Summary

Param unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ParamUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The param XML element. |
| paramType | System.String | The paramter type corresponding to the param XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `param`. |

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the param XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The param XML element list. |
| paramTypes | System.Collections.Generic.IEnumerable{System.String} | The paramater type names. |

## Program

##### Namespace

Vsxmd

##### Summary

Program entry.

### Main `method`

##### Summary

Program main function entry.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| args | System.String[] | Program arguments. |

## ReturnsUnit

##### Namespace

Vsxmd.Units

##### Summary

Returns unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ReturnsUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The returns XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `returns`. |

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the returns XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The returns XML element. |

## SummaryUnit

##### Namespace

Vsxmd.Units

##### Summary

Summary unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `SummaryUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The summary XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `summary`. |

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the summary XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The summary XML element. |

## TypeparamUnit

##### Namespace

Vsxmd.Units

##### Summary

Typeparam unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `TypeparamUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The typeparam XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `typeparam`. |

### ToMarkdown `method`

Inherit documentation from parent.

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the param XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The param XML element list. |