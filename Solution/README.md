### Correcting a Race Condition

**Branch name:** introthreads-prework

**RDE workfows:**
* `rde wflow run introthreads-prework-sleepandrace-warehouseapp`
* `rde wflow run introthreads-prework-sleepandrace-warehouseapptest`

Expected time required: 15 min

In this stage of some warehouse software we're developing, we are trying to track where packages are
being sorted. However there is a race condition between the `main` thread and a thread started in
`WarehouseManager` that are causing packages to be assigned to the wrong areas. As a quick fix we
want to implement `Thread.sleep()` to correct the race condition.

The steps to be completed are as follows:

1. Complete `sleepThread()` in `WarehouseApp` so it can pause the `main` thread. (The thread should sleep for 1 second.)
2. Identify where the race condition is happening, and use `sleepThread()` to correct it.

We currently have three lists of `WarehousePackage` objects: packages marked as High Priority,
packages containing books, and the remaining packages. After the list of packages are printed, the
output should be as follows:

- High Priority packages should should be in the High Priority list, *regardless of contents.*
- Any remaining books should be in the book list.
- Any remaining packages should be in the remaining list.
- There shouldn't be more packages than printed from the truck.

HINTS:
* [How do I find the race condition?](hints/hint-01.md)
