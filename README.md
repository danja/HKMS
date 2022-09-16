# Hyperdata Knowledge Management System

**_celebrating 20 years of vapourware_**

[doc in progress 2022-09-16]

Hyperdata Knowledge Management System (HKMS) is the current working title of a personal project I've been working on for a long time.

Skip down to '**Components**' if you wish to avoid the ramblings of an old man.

## WayBack

HKMS's first incarnation was [Ideagraph](https://web.archive.org/web/20040321215405/http://www.ideagraph.net/), intended as a _Personal Knowledge Management System_.

![screenshot](https://github.com/danja/HKMS/blob/main/images/ideagraph-1.gif?raw=true)

Its purpose was :

- idea brainstorming and development
- idea communication
- knowledge sharing
- project planning
- document organization
- semantic web blogging
- syndicated news reading, processing and republishing

That might sound like an outrageously wide scope, especially for a lone coder. It was, but it was surprising how far I got in a relatively short period of time as an unexceptional coder. The nearest it got to being finished was the desktop Java app in the screenshot above ([other screenshots](https://web.archive.org/web/20040402085138/http://www.ideagraph.net/2003-06/screenshots.htm)).

The reason this even remotely possible was that all of these things could share many common components. Critically, they could share the same data model.

### The Data Model

_A little personal history for context. I'd been interested in AI since seeing_ [2001 A Space Odyssey](<https://en.wikipedia.org/wiki/2001:_A_Space_Odyssey_(film)>) _as a kid, reading Asimov books. I got into electronics and computing as a teenager._ _My first computer was a [Commodore PET](https://en.wikipedia.org/wiki/Commodore_PET) onto which I once typed in a Tick-Tack-Toe AI from a magazine. Years later, at University, I took modules in neural nets and expert systems._ _Later still, I got online and had a day job at a college that included looking after the network, user support, database admin etc. But it did give me machines to play with_

_Around 1999 I stumbled upon. This seemed to connect the dots between the interesting AI bits and the Web. At the time I was clueless at both ends, but the rdf-dev mailing list was very friendly, and I gradually picked bits up._

The _Resource Description Framework_ [RDF](https://www.w3.org/RDF/) is a set of models and syntaxes for expressing arbitrary data in a form that is natively compatible with the Web. A clue is in the name : **Resource** in this context is the same as the **R** in [URL](https://en.wikipedia.org/wiki/URL). A resource is simply anything that you can identify. A real-world thing, a concept, or more typically on the Web, a document. The neat trick that RDF brings to the table is that you can also identify relationships between things and treat them as resources in their own rights.

Given a model that can identify things and describe relationships between them, you can build networks of information, more commonly known as **knowledge graphs**. These are versatile enough to be able to express pretty much any can of data you might wish to use on a computer. The practicalities of this can get a bit involved depending on what you're trying to do, but conceptually it's trivial.

Looking back at the list I had for Ideagraph : ideas, projects, blogs, documents... - all things expressible in RDF. Together, standard Java (using Swing for UI) and the nascent [Apache Jena](https://jena.apache.org/) framework had all the tools I needed to code something up.

### Views

RDF provides a model that can represent pretty much anything. It has various serialization formats so the data can be put in text. But like CSV files, this isn't very user-friendly.

So I wanted to make visualizing and editing RDF a lot more user friendly. In Ideagraph I had three main ways of looking at the RDF:

- text - view source of a particular bit of the RDF, or view/edit a text description that was a property of a node
- tree - a collapsible tree view, similar to those used in file explorers (loops would just keep expanding)
- graph - a node & arc nextwork view

I can't remember how far I'd got with implementation, but I also had more dedicated views for :

- Project - a view structure around a [vocab](https://hyperdata.it/xmlns/project/index.htm) designed for describing projects
- Channels - for RSS feeds
- Vocabs - for RDFS
- Commands - an interpreter (I forget what I used for this, may have been an ad hoc DSL or some standard language interpreter)
- Settings

## Lessons

scope drift

too generic

## Decoupling

- [Gradino](https://github.com/danja/Gradino) : RDF-backed blog engine, Java/Scala (retired)
- [Seki](https://github.com/danja/seki) : (retired)

- [Scute](https://github.com/danja/Scute) : a Semantic Web hacking tool, desktop Java (retired)

## Components

- [NewMonitor](https://github.com/danja/NewsMonitor) : quasi-intelligent feedreader/aggregator, Java backend
- [FooWiki](https://github.com/danja/foowiki) : a browser-based, SPARQL Server-backed Wiki

* [Thiki](https://github.com/danja/thiki) : RDF-backed personal Wiki for Android devices

- [Foolicious](https://github.com/danja/foolicious) : a SPARQL-backed bookmark manager (del.icio.us clone)

* [SparqlPress](https://github.com/danja/sparqlpress2)
* [Trellis](https://github.com/danja/trellis) : SPARQL-backed hierarchical to-do list
* [Schema Editor](https://github.com/danja/schema-editor) : browser-based RDF schema authoring tool
* [Diced](https://github.com/danja/Diced)

[SPARQL Diamonds](https://github.com/danja/sparql-diamonds)

demos :
https://hyperdata.it/sparql-diamonds/

link scraper - PWA

markdown

mobile

## Current (and Future) Directions

Bookmark manager : the one in eg. Chrome browser is absolutely hopeless
