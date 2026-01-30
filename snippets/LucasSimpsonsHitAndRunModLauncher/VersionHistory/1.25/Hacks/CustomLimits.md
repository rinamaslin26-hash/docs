* Added a `[Missions]` section with a new `StageLimit`. 
* Added a `[Pedestrians]` section with a new `GroupLimit`.
	* Also moved the `[Miscellaneous]` section's `PathLimit` here.
		* It is still supported in the `[Miscellaneous]` section for backwards compatibility.
* Fixed an issue where the `[Regions]` section's `Limit` has been broken since its introduction in Version 1.15 on September 20th, 2016.
	* The actual mistake was due to the hack mistakenly changing the memory allocator used for regions.
	* This happened because these happen to use heap 7 (`GMA_LEVEL_ZONE`) and since the default region limit is 7, this number was also mistakenly being changed by this hack in every previous version where this feature exists.
	* This update also removes a hard limit of 127 from this limit, however it was impossible to actually set it anywhere near that number due to this mistake.