# Changelog

## v5.0a – 2024-06-19

- The package status has been changed to ‘unmaintained’.


## v5.0 – 2018-01-10

- `\gantttitlecalendar` now recognizes the `decade` key.
- Key `compress calendar` has been replaced by `time slot unit` to allow an additional level of compression (year).
- The command `\ganttvrule` allows to draw general vertical rules (similar to the today rule). The keys `vrule`, `vrule offset`, `vrule label font` and `vrule label text` configure those rules.
- The key `expand chart` was added, which specifies that a chart should expand horizontally to a given dimension.
- The key `title label text` was added to allow fine-tuning of title label formatting.
- Made `pgfgantt` robust to `amsgen`'s redefinition of `\@ifstar`.


## v4.0 – 2013-06-01

- The key `link label anchor` was renamed to `link label node`.
- `\newganttchartelement` defines completely new chart elements.
- The key `progress label anchor` was replaced by `bar/group/milestone progress label node`.
- The keys `bar/group/milestone progress label anchor` were added.
- The key `progress label font` was replaced by the keys `bar/group/milestone progress label font`.
- The key `incomplete` was removed.
- The keys `group right/left peak` and `group peaks` were replaced by `group right/left peak tip position`, `group peaks tip position`, `group right/left peak width`, `group peaks width`, `group right/left peak height` and `group peaks height`.
- Chart elements are now nodes, so the corresponding styles must specify a node shape.
- The key `time slot modifier` was renamed to `chart element start border`.
- The keys `bar/group/milestone label inline anchor` were renamed to `bar/group/milestone inline label node`.
- The keys `bar/group/milestone label shape anchor` were renamed to `bar/group/milestone inline label anchor`.
- The keys `bar/group/milestone label anchor` were renamed to `bar/group/milestone label node`.
- The key `title label anchor` was renamed to `title label node`.
- `\gantttitlecalendar` prints a title calendar.
- The keys `calendar week text` and `compress calendar` were added.
- The key `newline shortcut` determines whether the shortcut for line breaks is defined in the chart. In this case, `\ganttalignnewline` allows line breaks in the node text.
- The keys `today offset`, `today label font` and `today label node` were added.
- The key `today` accepts a time slot specifier.
- The canvas is now a node with shape `rectangle` by default.
- `\newgantttimeslotformat` allows the user to define custom time slot formats.
- The key `time slot format/start date` specifies the internal date representation of digit 1 in the `simple` time slot format.
- The key `time slot format/base century` provides the century for autocompletion of two-digit years.
- The key `time slot format` changes the format of time slot specifiers.
- The `ganttchart` environment now requires two mandatory arguments.


## v3.0 – 2012-01-25

- `\setganttlinklabel` specifies the label for all links of a certain type. The `link label` key locally overrides any label set by this command.
- The `chart element` shape supports four additional anchors (`on left`, `on top`, `on right` and `on bottom`).
- `\@gtt@get` has been renamed to `\ganttvalueof` to provide a convenient access for link type authors.
- `\@gtt@keydef` and `\@gtt@stylekeydef` have been rewritten to support `pgfkey`'s abilities to store key values.
- New auxiliary macros for `\newganttlinkstyle`: `\xLeft`, `\xRight`, `\yUpper`, `\yLower`, `\ganttsetstartanchor`, `\ganttsetendanchor` and `\ganttlinklabel`.
- Completely rewrote the code for links (again). Definition of new link types is now possible (via `\newganttlinktype` and `\newganttlinktypealias`).
- The `bar/group/milestone label shape anchor` keys allow for a fine-tuned placement of chart element labels.
- All style keys (`canvas`, `bar` etc.) only support the common TikZ style key syntax.


## v2.1 – 2011-11-10

- The `inline` key moves labels close to their respective chart elements.
- Added three keys (`bar/group/milestone label inline anchor`) for placing inline labels.
- The `ganttchart` environment may be used outside a `tikzpicture`.
- The syntax of `\ganttlink` was completely changed. The command now takes one optional and two mandatory arguments. The latter specify the name of the chart elements to be linked. Consequently, the keys `b-b`, `b-m`, `m-b` and `m-m` were removed. The keys `s-s`, `s-f`, `f-s` and `f-f` are now values for the `link type` key.


## v2.0 – 2011-10-10

- The optional argument of `\ganttnewline` now also accepts a style.
- Removed the `hgrid shift` and `last line height` keys.
- Removed the `vgrid lines list` key, as its behaviour can be simulated by an appropriate `style list` for `vgrid`.
- Added style lists for the horizontal and vertical grid.
- Removed the `vgrid style` key.
- Completely rewrote the calculation of coordinates.
- The `x unit`, `y unit title` and `y unit chart` keys specify the width of time slots and the height of title or chart lines, respectively. Thus, one can draw titles whose height differs from the rest of the chart. Furthermore, the x- and y-dimensions of the chart are independent of the dimensions of the surrounding `tikzpicture`.


## v1.1 – 2011-04-18

- `link tolerance` decides whether a five- or a three-part link is drawn.
- `milestone label text` configures the text of a milestone label.
- `bar label text` configures the text of a bar label.
- The `time slot modifier` key has been added. If set to zero, all x-coordinates are interpreted as given, without regarding them as time slots.
- The `vgrid lines list` key determines the number of vertical grid lines drawn.
- The introduction clarifies what is meant by "a current `pgf` installation".
- `group label text` configures the text of a group label.


## v1.0 – 2011-03-01

- initial release
