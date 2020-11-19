# st - simple terminal

st is a simple terminal emulator for X which sucks less.

### Installation

```sh
$ git clone https://github.com/curzes/st.git
$ cd st
$ make clean
$ make
$ sudo make install
```
### Patche

***st-alpha-0.8.2.diff***

This patch allows users to change the opacity of the background. Note that you need an X composite manager (e.g. compton, xcompmgr) to make this patch effective.

***st-bold-is-not-bright-20190127-3be4cf1.diff***

In st, bold text is rendered with a bold font in the bright variant of the current color. This patch makes bold text rendered simply as bold, leaving the color unaffected.

***st-clipboard-0.8.3.diff***

This trivial patch sets CLIPBOARD on selection, the same as your browser.

You may want to replace selpaste with clippaste in your config.h bindings to complete the affect.


***st-scrollback-20200419-72e3f6c.diff***

Scroll back through terminal output using Shift+{PageUp, PageDown}.

***st-scrollback-mouse-20191024-a2c479c.diff***

Apply the following patch on top of the previous to allow scrolling using Shift+MouseWheel.

Apply the following patch on top of the previous two to allow scrollback using mouse wheel only when not in MODE_ALTSCREEN. For example the content is being scrolled instead of the scrollback buffer in less. Consequently the Shift modifier for scrolling is not needed anymore.

***st-selectioncolors-0.8.4.diff***

This patch adds the two color-settings selectionfg and selectionbg to config.def.h. Those define the fore- and background colors which are used when text on the screen is selected with the mouse. This removes the default behaviour which would simply reverse the colors.

Additionally, a third setting ingnoreselfg exists. If true then the setting selectionfg is ignored and the original foreground-colors of each cell are not changed during selection. Basically only the background-color would change. This might be more visually appealing to some folks.

***st-vertcenter-20180320-6ac8c8a.diff***

Vertically center lines in the space available if you have set a larger chscale in config.h.

### Colors
_coming soon_

Black

Pink

Orange

Green

Gray
