Fixed a crash on startup that occurred with certain game executables in certain circumstances:
* If the mod used the `Locator` attribute on a `Selector` element inside a `PhoneBooth` element.
* If the mod used a `Car` element inside a `FreeItems` element inside a `PhoneBooth` element.