* Added a `Not` property on conditions that makes them return true when they are not met.
* Made the `BonusMission` property on `Mission` type `[Condition]` sections work as originally documented.
    * This value was documented as being a number from 1 to 5.
    * All previous versions were checking for 21 to 25 instead of 1 to 5.
    * For backwards compatibility reasons, it now checks for either set of numbers.