# SESSION

Session is a tool for social computation. 

If git lets us code together, Session lets us compute together.

More tangibly, it is a web-based clojure repl that stores the repl history in Datomic. 

Session lets you do data analysis, produce web content, stand up systems, and interact with services. You do those things by entering code and receiving results, which could be just data, but may also be things like graphics or interactive web content.

Importantly, Session also records the history of your actions and results. So you can come back to it, and see what happened. Or share it with others, so they can repeat it, or extend and adapt your work. 

Sessions can serve as templates, extension points, audit trails, documentation, or CMS components. They are a form of accretive, executable knowledge. 

Like source code, sessions can be incrementally authored by one person, or by a community. Session is the equivalent of git for computations.

Like git, the core of Session is an immutable datastructure.

Git demonstrated the importance of immutable data as the basis of peer networks. Immutable data facilitates exchange.

Session uses Datomic as this core datastructure.

The first key element in Session is storing not just the code, but also the result. Storing both means remembering what happened.

The second key element is the web UI. Being on the web means being able to create & distribute interactive content. It means integrating human-operated computation into our communications network.

The third key element is delegating to services for the actual computations. Delegation means having the full power of our existing sytems, wrapped up in a more convenient package.

This combination of features lets Session create easily shareable computations of arbitrary power.

In a sense, Session facilitates the interplay between human and machine computation. The computation of the human is to take the state of the world, and produce the next instruction. The computation of the machine is to execute the instruction and display the result in context.

If this process can be made location independent, then the computation can be constructed socially, with any number of participants bringing their ideas and computational resources to the table.

We will know social computation has arrived when we are the causes and effects of each other's computations.

Currently alpha quality software, use at your own risk :)

See [Architecture](https://github.com/kovasb/session/wiki/Architecture) for a description of components and how they come together.

# Usage

First, compile the javascript:

    lein cljsbuild once

To invoke session with a default datomic db and nrepl server:

    lein run

Then direct the browser to localhost:8090 . (Only verified to work with Chrome)

You can override the various defaults with your own uri's and ports:

    lein run '{:port <session-web-client-port> :datomic-uri "<your-datomic-uri>" :nrepl-uri "<your-nrepl-uri>"}'

For persistent results, you'll likely want set up and use a transactor with local storage.

To create input areas, mouse around the UI untill a right arrow appears, and click. An input area should appear.

To evaluate input, hit shift-enter.

## License

Copyright (C) 2012 Kovas Boguta

Distributed under the Eclipse Public License, the same as Clojure.
