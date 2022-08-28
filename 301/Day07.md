Q) Who is Roy Fielding?

he helped write the first web servers, that sent documents across the internet… and then he did a ton of research explaining why the web works the way it does. His name is on the specification for the protocol that is used to get pages from servers to your browser.

Q) Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?

Because they weren't designed to be used like that. When Fielding and his colleagues started building the web, being able to talk to any machine anywhere in the world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didn't have those requirements. You just needed to talk to a small group of machines.

Q) What is the HTTP protocol that Fielding and his friends created?

The protocol I mentioned, that he helped write, HTTP, it's capable of all sorts of neat stuff that people ignore for some reason.

Q) What does a GET do?

get the page

Q) What does a POST do?

If a system wants to replace something in another system, it uses an HTTP verb of PUT, or, to do a partial update, it'll hopefully use PATCH. The only thing left to figure out is what the data models should look like.

Q) What does PUT do?

system wants to replace something in another system, it uses an HTTP verb of PUT

Q) What does PATCH do?

for updating

all API is ready
