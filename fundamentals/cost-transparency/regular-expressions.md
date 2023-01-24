# Regular Expressions

Cloudthread platform allows for use of **regular expressions (regex)** in filter conditions in [costs-overview.md](costs-overview.md "mention") as well as in [unit-metric.md](../unit-metrics/unit-metric.md "mention") sections.

We support 2 types of regex filtering:

* `IN` conditions (single choice): POSIX-style regex
  * `^abc.*`
  * [https://quickref.me/regex](https://quickref.me/regex)
  * Case sensitive
* `LIKE` conditions (bulk select): database `LIKE` statement pattern matching
  * `%abc%`
  * [Example](https://www.postgresql.org/docs/current/functions-matching.html#FUNCTIONS-LIKE) for Postgres
  * Case sensitive
