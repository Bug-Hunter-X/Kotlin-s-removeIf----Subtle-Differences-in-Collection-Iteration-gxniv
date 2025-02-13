# Kotlin's removeIf(): Subtle Differences in Collection Iteration

This repository showcases a subtle difference in how the `removeIf` function operates across various Kotlin collection types (Lists, Maps, and Sets).  While generally straightforward, the underlying implementation details can lead to unexpected results if not fully understood.

## Bug Description
The `removeIf` function removes elements from a collection based on a predicate.  However, depending on the collection type (mutableList, mutableMap, mutableSet),  the iteration and element removal can vary, potentially resulting in unexpected behavior or errors. The primary concern lies in modification during iteration which can produce unexpected results and skip elements under certain conditions.