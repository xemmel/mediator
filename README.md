# Mediator

## Current version

1.7

## Parameters

### Syntax

```
[[method]=[replace],[search]=[morten],[replace]=[mogens]],[[method]=[replace],[search]=[mogens],[replace]=[clara]]

```
[Back to top](#mediator)

## Processes

### ConditionalHtmlToJsonProcess

#### Syntax

```
[method]=[conditional_htmltojson]

```

[Back to top](#mediator)

### PromoteStatusCodeProcess

#### Syntax

```
[method]=[promotestatuscode],[exclude]=[405|200,404|202]

```

#### Parameters

Name|Description|Required|sample
----|-----------|--------|-----
exclude|delimited string with the codes to exclude/translate||405\|200,404\|202
promotefault| **promotes** IsFault if responseCode is fault||true
setfaultschema|sets SchemaStrongName to soapfault **if** fault||true
outputstatuscode|if set to 0 set OutboundHttpStatusCode to the responseCode otherwise set it to a hardcoded int||500

[Back to top](#mediator)

### Binding_JsonToXMLProcess

#### Syntax

```
[method]=[binding_jsontoxml]

```

#### Parameters 

Name|Description|Required|sample
----|-----------|--------|-----
rootname|the root name of the output xml (note: needed if json does not have a root element||Response
namespace|the namespace of the output xml||http://ff
promotefault|boolean to specify if IsFault should be promoted||true

[Back to top](#mediator)

### Replace

#### Syntax

```
[method]=[replace],[search]=[morten],[replace]=[mogens]

```

#### Method Name

```
replace
```

#### Parameters

Name|Description|Required
----|-----------|--------
search|the string pattern to search for|*
replace|the string pattern to replace wit|*


### MapXMLProcess

#### Syntax

```
[[method]=[mapxml],[xsltpath]=[c:\temp\map.xslt]]

```

#### Parameters

Name|Description|Required
----|-----------|--------
xsltpath|path for the xslt|*

