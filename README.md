**include.js**
<br/>Copyright 2016, Morgan McGuire [@CasualEffects](https://twitter.com/CasualEffects)
<br/>http://casual-effects.com

Adds a client-side include statement for HTML. To use:

 1. Put `<script src="include.min.js"></script>` in both the parent and child documents
 2. Use `<include src="child.html"></include>` wherever you want to include another document

Features:
 - Works recursively
 - Works with multiple inclusions of the same source
 - Fixes relative URLs in other tags (mostly)
 - Supports CSS
 - Also works for purely-static sites
 - Also works for local files and across domains
 - Secure (both the parent and child document must opt-in with a script tag)

Limitations:
 - Doesn't bother checking for infinite recursion (just don't do that!)
 - Relative URLs within _inline_ style tags/attributes and Javascript 
   will break, if files are in different directories

Alternatives:
 - PHP server-side inclusion (requires a nonstatic server, breaks relative URLs)
 - script tags with a lot of document.write calls (ugly)
 - iframes (break document flow and styling)
 - XMLHttpRequest tricks (cross-domain and local/chrome problems)
