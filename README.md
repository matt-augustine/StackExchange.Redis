StackExchange.Redis
===================

StackExchange.Redis is a high performance general purpose redis client for .NET languages (C# etc). It is the logical successor to [BookSleeve](https://code.google.com/p/booksleeve/),
and is the client developed-by (and used-by) [Stack Exchange](http://stackexchange.com/) for busy sites like [Stack Overflow](http://stackoverflow.com/). For the full reasons
why this library was created (i.e. "What about BookSleeve?") [please see here](http://marcgravell.blogspot.com/2014/03/so-i-went-and-wrote-another-redis-client.html).

Note: this release should be considered "beta": the API may be subject  to minor changes.

Features
--

- High performance multiplexed design, allowing for efficient use of shared connections from multiple calling threads
- Abstraction over redis node configuration: the client can silently negotiate multiple redis servers for robustness and availability
- Convenient access to the full redis feature-set (caveat: scripting is still outstanding)
- Full dual programming model both synchronous and asynchronous usage, without requiring "sync over async" usage of the [TPL][1]
- Support for redis "cluster"

Installation
---

StackExchange.Redis can be installed via the nuget UI (as [StackExchange.Redis](https://www.nuget.org/packages/StackExchange.Redis/)), or via the nuget package manager console:

    PM> Install-Package StackExchange.Redis

Documentation
---

- [Basic Usage](https://github.com/StackExchange/StackExchange.Redis/blob/master/Docs/Basics.md) - getting started and basica usage
- [Keys, Values and Channels](https://github.com/StackExchange/StackExchange.Redis/blob/master/Docs/KeysValues.md) - discusses the data-types used on the API
- [Transactions](https://github.com/StackExchange/StackExchange.Redis/blob/master/Docs/Transactions.md) - how atomic transactions work in redis

  [1]: http://msdn.microsoft.com/en-us/library/dd460717%28v=vs.110%29.aspx
