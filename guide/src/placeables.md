# Placeables

Text in Fluent may use special syntax to incorporate small pieces of
programmable interface. Those pieces are denoted with curly braces `{` and
`}` and are called placeables.

It's common to use placeables to interpolate external
[variables](variables.html) into the translation. Variable values are
provided by the developer and they will be set on runtime. They may also
dynamically change as the user uses the localized product.

```
# $title (String) - The title of the bookmark to remove.
remove-bookmark = Really remove { $title }?
```

It's also possible to [interpolate other messages and terms](references.html)
inside of text values.

```
-brand-name = Firefox
installing = Installing { -brand-name }.
```

Lastly, placeables can be used to insert [special characters](special.html)
into text values. For instance, due to placeables using `{` and `}` as
delimiters, inserting a literal curly brace into the translation requires
special care. Quoted text can be effectively used for the purpose:

```
opening-brace = This message features an opening curly brace: {"{"}.
closing-brace = This message features a closing curly brace: {"}"}.
```
