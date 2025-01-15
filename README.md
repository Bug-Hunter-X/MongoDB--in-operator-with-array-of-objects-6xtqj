# MongoDB $in operator with array of objects
This repository demonstrates an uncommon error related to the usage of the `$in` operator in MongoDB queries with arrays of objects. The incorrect query may not return the expected results. The solution provides the correct way to construct the query.

## Bug
The bug lies in how the `$in` operator is used when querying for documents containing arrays of embedded objects.  Using `$in` directly on such objects will not yield the expected results. The correct approach involves using the `$elemMatch` operator.

## Solution
The solution replaces the incorrect usage of `$in` with the `$elemMatch` operator, enabling proper matching of documents based on the subfield values within the embedded objects.