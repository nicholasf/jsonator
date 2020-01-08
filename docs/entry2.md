
# Designing the JSONator.

Out of interest I used a system definition language called Sysl (https://github.com/anz-bank/sysl/). 


points:

* I couldnt work out how to depict internal calls in a service. I guess this tool wants to depict service to service dependencies.
* There seems to be a lot of depth in the pet shop syntax example, I just took a simple and quick approach to get started.
* diagram generation just worked.
* feels like a nice way to rapidly build 

There were some parts I wondered about depicting, for example, should I really write out the behaviours for subscribing to a queue or represent transactional if/then logic when I depicted a database write?

To generate the Sequence Diagram:

sysl sd -o "sequence.png" -s "Sink <- Receive" sysl/jsonator.sysl


The Integration diagram took a little bit of guesswork when configuring the Project stanza, but not much.

sysl ints -o integration.png --project Project sysl/jsonator.sysl

The Data Model

I ran into a bug with this, had to open a ticket.
