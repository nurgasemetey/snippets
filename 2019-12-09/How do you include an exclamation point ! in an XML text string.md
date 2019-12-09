### How do you include an exclamation point ! in an XML text string


[XML How do you include an exclamation point ! in an XML text string? escape sequence? - Stack Overflow](https://stackoverflow.com/questions/14468549/xml-how-do-you-include-an-exclamation-point-in-an-xml-text-string-escape-sequ "XML How do you include an exclamation point ! in an XML text string? escape sequence? - Stack Overflow")




```shell
An XML file should accept a exclaimation point, except possibly immediately after a open angle bracket.

If it really refuses, you should be able to use a numeric entity: Help&#x21; = Help!

Or you can get verebose <![CDATA[Help!]]>
```
