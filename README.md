lineage
=======

Family Tree Data Expression Engine

See a live demo at
http://www.bengarvey.com/lineage


## Configuration

All configuration is done in the `config.json` file.
This is what its keys do:

### `data`
Points to the JSON-file containing your data.
Per default, this points to the example file located at
`data/familyData.json`.

### `filter`
In the web view's menu bar you can filter for specific names using the provided
input field.
This key allows you to set an initial filter which will be active when the web
view is freshly loaded.

### `startYear`
StartYear

### `endYear`
EndYear

### `speed`
How many milliseconds does one year take when you hit the "Play" button?
Default value is 100 which makes 10 years pass per second
(100ms = 1/10th of a second).

### `menuDefaultOpen`
If this is set to `true`, the menu is instantly opened when the web view is
loaded.
Defaults to `true`.

### `debug`
This key is irrelevant to the observable behavior of lineage and only affects
the logging which happens in the background.

### `showDead`
If this is false, only people who are alive at the time of the currently active
year are shown in the graphs.
If it's true, everybody who has been born at this time (regardless of death
date) is shown.


## Notes
- For viewing large datasets, it may help to zoom out your browser
- If you lose the ui, move your mouse to the edge of the screen at the top left
- To run the demo in play mode, just press play and watch the years tick by
- To hear the music, check the music checkbox and press play
- To see the full dataset in the demo, remove all the names from the search /
    filter box


## Upcoming features / ToDo
- Move to D3v7?
- Add favicon
- Pause music when the music checkbox is unchecked while the timeline is running
- New key in config: `mode` -> Which mode (tree, timeline, cluster) is displayed
    by default?
- Find better name for key `speed` in config. `yearDuration`?
    Or change functionality (e.g. use `1 / speed ` instead of `speed` in loop)
    to reflect key name?
- Add a config key for the constant `searchRadius` in lineage.js
