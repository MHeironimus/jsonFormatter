# jsonFormatter - jQuery Plugin
A jQuery Plugin that formats JSON strings.

This jQuery plugin is based on a nice little JavaScript routine written by Vladimir Bodurov that can be viewed at [http://bodurov.com/JsonFormatter/](http://bodurov.com/JsonFormatter/).

To use this plugin include jsonFormatter.min.css and jsonFormatter.min.js in your html file. See the jsonFormatterExample.html file for an example on how to do this. If you wish to use the darkTheme, include the jsonFormatter-darkTheme.min.css file.

## Documentation
### .jsonFormatter(options)
**Returns**: jQuery

**Description**: If the matched elements contain JSON, they are formatted to be easier to read. Arrays and object are optionally collapsible.

### Options
#### quoteKeys
**Type**: Boolean
**Default**: true

Specifies if object's keys should be quoted in the formatted output.

#### collapsible
**Type**: Boolean
**Default**: true

Specifies if arrays and objects are collapsible in the formatted output.

#### hideOriginal
**Type**: Boolean
**Default**: true

Specifies if the original element is hidden. The element will only be hidden if it contains valid JSON that was successfully formatted.

## Example
```
<html>
<head>
    <title>jsonFormatter Example</title>
    <link href="../source/jsonFormatter.min.css" rel="stylesheet" />
</head>
<body>
    <div class="content">
        <h1>jsonFormatter Example</h1>
        <section>
            <h2>Default Theme, Default Options Example</h2>
            <div class="exampleJavaScript">$('.jsonFormatter').jsonFormatter();</div>
            <div class="exampleJson jsonFormatter">{stringValue:"string value",numberValue:-4.506,booleanValue:true,arrayOfStrings:['one','two','three'],arrayOfObjects:[{firstProperty:1,secondProperty:2},{firstProperty:3,secondProperty:4}],undefinedProperty:undefined,emptyProperty:{}}</div>
        </section>

    <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.11.2.min.js" type="text/javascript"></script>
    <script src="../source/jsonFormatter.min.js" type="text/javascript"></script>
    <script type="text/javascript">
        $(document).ready(function () {
            $('.jsonFormatter').jsonFormatter();
        });
    </script>

</body>
</html>
```