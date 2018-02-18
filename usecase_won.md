# Use Case: Web of Needs

[Web of Needs (WoN)](https://matchat.org/) lets users post RDF structures to describe their interest in interactions. 

Independent matchers find posts (=needs) that may be suitable for an interaction and send 'hint' messages to the postings, which can be seen by the users.

Users can then start communicating by exchanging messages that can contain arbitrary RDF.

Thus, we have 4 main points where we'd like to use rdfruit:
## 1. Create Posting
Generate arbitrary RDF, ideally using the perfect user friendly GUI.

Example: I want to get from my current location to point B

## 2. Display a Posting when matched 
Render a GUI from a priori unknown RDF, ideally in a way that fits the user's context

Example: Someone is nearby and would drive me to B if I'm quick enough to hop on within 3 minutes.

## 3. Author a message 
Generate arbitrary RDF, ideally using the perfect user friendly GUI.

Example: confirm an appointment: in 3 minutes at location A

## 4. Display a message 
Render a GUI from a priori unknown RDF, ideally in a way that fits the user's context

Example: Show that the other user has confirmed my suggestion for an appointment in 3 minutes at location A


## Requirements for the UI Layer
### 1. Discovery of UI components
In WoN, you can post and find anything. The only thing you'll know about postings or messages a priori is that they are RDF datasets. They will have a few standard triples, but these don't normally interest users. Consequently, it is not feasible to prepare a UI library for authoring every conceivable WoN posting. Rather, we'd like a discovery system that finds the right UI component on the fly. For that to be possible, the components need to be adaptive in terms of visual style, language, context (whatever that is exactly - it is a thing). Moreover, the components must not pose a security risk in any way.

### 2. Generic RDF authoring capabilities
For situations in which no GUI components can be found, generic tools are needed for content authoring. The requirements for those components are the same as in 1. In addition to that, the generic tools should allow non-RDF savvy Web users to author simple RDF structures.

