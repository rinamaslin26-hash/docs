* Added the `DeletedEntityLimit` property to the `[Miscellaneous]` section.
* Added the `PathLimit` property to the `[Miscellaneous]` section.
* Fixed an issue where changing the `Intersection` limit to higher than normal did not change the amount of animated arrows that got created.
    * This caused crashes since there's supposed to be an instance of the arrows created for every intersection.