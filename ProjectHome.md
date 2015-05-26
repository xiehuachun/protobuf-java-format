# Description #
Provide serialization and de-serialization of different formats based on [Google’s protobuf](http://code.google.com/p/protobuf/) Message.
Enables overriding the default (byte array) output to text based formats such as XML, JSON and HTML.

# Example #
For XML output, use `XmlFormat`
```
Message someProto = SomeProto.getDefaultInstance();
String xmlFormat = XmlFormat.printToString(someProto);
```

For XML input, use `XmlFormat`
```
Message.Builder builder = SomeProto.newBuilder();
String xmlFormat = _load xml document from a source_;
XmlFormat.merge(xmlFormat, builder);
```

For Json output, use `JsonFormat`
```
Message someProto = SomeProto.getDefaultInstance();
String jsonFormat = JsonFormat.printToString(someProto);
```

For Json input, use `JsonFormat`
```
Message.Builder builder = SomeProto.newBuilder();
String jsonFormat = _load json document from a source_;
JsonFormat.merge(jsonFormat, builder);
```

For HTML output, use `HtmlFormat`
```
Message someProto = SomeProto.getDefaultInstance();
String htmlFormat = HtmlFormat.printToString(someProto);
```

# What's next? #
  1. Smile format [Spec](http://wiki.fasterxml.com/SmileFormatSpec)
  1. Support de-serialization for HTML/xHTML
  1. Add Support for RSS/Atom
  1. Add Support for [YAML](http://www.yaml.org)
  1. Additional output types?