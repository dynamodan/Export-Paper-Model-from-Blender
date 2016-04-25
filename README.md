# Export-Paper-Model-from-Blender
Python addon for creating plywood tab-and-notch CNC outlines in Blender 2.7 (development version)

This is forked from addam's excellent "Export Paper Model from Blender" add-on.  I have extended it by adding an option called "Create Plywood Tabs" to produce tabbed-and-notched islands for CNC- or laser-cut plywood.  It's still rudimentary and assumes the thickness of the plywood is the same as what you set the "Tabs and Text Size" to.  (That's the most likely assumption anyways.)

There is also an option to set the "Plywood tab ratio" which is the ratio of the tab (and corresponding notch) width to its height. It enables you to control how fine the tabs are (default is 3 to help avoid the "zipper" look).

The new tabbing code also features notch depth compensation based on the edge angles.  It will make the notch shallower as the angle increases, and finally eliminate the notch altogether when the angle is acute or greater (tabs are still produced and will interlock correctly).  With this feature, your edge joints will mesh together only as deep as they should, allowing you extra glue contact (and no gap) where each tab "bottoms out" in its notch.

Known issue: The resulting structure's "radius" will be bigger than the original object by the thickness of the material.  It's also completely unknown what the result is of concave shapes, if the shapes will even fit at all.  They may very well be off by one or more thicknesses of the material.  I have not yet tested to determine this.

This code comes without any kind of guarantee of accuracy, or any support whatsoever.
