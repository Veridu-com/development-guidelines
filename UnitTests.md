# Unit Tests
Unit Testing isn't the holy grail of development, but is a very handy tool to spot issues on projects that are being actively developed by multiple people or that have to integrate into different systems, it also helps the developer to create decoupled code.

You are not required to do 100% code coverage, but you MUST ensure that _at least_ public and protected methods of every class/package are properly tested and that every integrating part of your project is properly tested (that includes integrations with databases, caching layers etc).

It's also important to note that a high code coverage percentage does not necessarily imply on a well tested code, so think of edge cases, "This will/should never happen" cases and for weakly typed languages test invalid type parameters/returns.

You MUST use standard tools for Unit Testing and MUST NOT create your own tooling.
