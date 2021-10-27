# OBS scenes

These are some scene collections for OBS.

## Principles

* Many scenes use a resolution of 840 (wide) × 1080 (high).  This
  weird resolution is actually carefully selected.
  * For interactive work, where a student will be following along, the
    follower will need plenty of screen space to do so.  A vertical
    share allows them to have half of their screen for following
    along.
  * 1080 is the height of a FullHD screen.
  * YouTube will re-encode HD versions at exactly this resolution -
    changing any number makes it not pixel-perfect.  YouTube doesn't
    re-encode perfectly at arbitrary aspect rations.
  * The rule of thumb is "present from your smallest screen".  This
    has the same effect.


* These scenes tend to insert external elements, for example logos.
  These logos are referred to by absolute pathname and *not* included,
  so the scenes need modification before they will actually work.  You
  may need

## Common names

To systematically control all scenes via the API, we need to
standardize some scene names.  (Note the terminology, **scene** is a
selectable layout, **sources** are items within the scene.)  We have done that here:

- `Title`: A general title card used for intros and so on.
  - `Clock`: (text that matches xx:NN, regex `([xX?]{2}:)(\d{2})(\s+|$)` )
- `Gallery`: The gallery of presenters, mostly full screen.
- `Local`: Local screenshare (of the local computer running OBS).
  - `_Camera`: includes people inserted
- `Remote`: Capture of remote screenshare (e.g. zoom screenshare
  window)
  - `_Camera`: includes people inserted
- `Notes`: A screen capture of HackMD or other shared notes.
  - `_Camera`:  includes people inserted
- `--`: this is a placeholder scene to separate primary scenes from
  the internal ones below.
- `_`-prefixed scenes: these are internal scenes which get inserted
  into other scenes.
  - `_Camera`: Scene with camera.  Re-inserted into the abve

## Included scenes

The following screens are included in this collection:

### Teaching_Streaming_ZoomCapture

This is used for livestreaming a course by capturing Zoom.


### Demo recording

This is designed for recording 840x1080 demos on your local computer.
It can also be used



## Status of this repository

Under development, reference but may not necessarily be useful to
anyone.

Right now updating is done by rkdarst updating in his own OBS and
re-exporting.
