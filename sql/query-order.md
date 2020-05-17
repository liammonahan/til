# SQL Query Order

What order do SQL queries run in?
In a non-image format, the order is:

    FROM/JOIN and all the ON conditions
    WHERE
    GROUP BY
    HAVING
    SELECT (including window functions)
    ORDER BY
    LIMIT


questions this diagram helps you answer

This diagram is about the semantics of SQL queries – it lets you reason through what a given query will return and answers questions like:

    Can I do WHERE on something that came from a GROUP BY? (no! WHERE happens before GROUP BY!)

    Can I filter based on the results of a window function? (no! window functions happen in SELECT, which happens after both WHERE and GROUP BY)

    Can I ORDER BY based on something I did in GROUP BY? (yes! ORDER BY is basically the last thing, you can ORDER BY based on anything!)

    When does LIMIT happen? (at the very end!)

[source](https://jvns.ca/blog/2019/10/03/sql-queries-don-t-start-with-select/)
