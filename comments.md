---
---
Comments
==========

Notice that this page appears to have a "Title". 

Look at the raw text and you will see the YAML section is blank, but below the YAML 
there is the Title: "Comments" followed by a line of "equals" signs. 

These equals signs appear to signal a Title has been entered. I have no idea
why this works the way it does, but whatever, someone certainly does. I happen
to have seen it on another page in someone elses' repo and tried it.

Also note that the YAML MUST be present, even if completely blank, or the pages will not render as HTML.
I kind of understand this concept. 

The YAML must be blank because none of the layouts or other things embedded in YAML
have been defined anywhere, so if you were to put something like `title:Comments` inside
the YAML, it would give an error (a fatal error IIRC).