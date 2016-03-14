How npm switch from a monolith
==============================

## [Slides](http://slides.com/seldo/cheating-galls-law#/)

## Laurie Voss (CTO at npm)

Gall's law, to write a complex system that works you have to start with a simple system that works.

They "cheated" Gall's law

> If you're really lucky, something terrible will happen: success

> Success: now scale it

Scale by growing the monolith? Scale by micro services?

Micro-services don't work because complexity

How to split effectively? CHEAT

How to cheat: by not rewriting the whole thing:

1. Slice a piece off into a module with a clearly defined interface
2. Then write a second implementation of that interface
3. Put a proxy in front and send requests to the second implementation (they used varnish, made npm way more reliable)
4. Replace proxy with a micro service
5. Now do it again (they extract authentication)
6. Repeat (variety of data stores depending on the needs!)
7. Original couch app is still there

Beat Gall's law with modularity aka information hiding

Each service still a simple system when in isolation

Working system every step of the way

Simple working first, then scale it later

Respect Gall: Rewrite in pieces

Be bold

120 seconds of downtime in all of 2015 while doing this due to a bad deploy
