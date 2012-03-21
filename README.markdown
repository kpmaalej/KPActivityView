KPActivityView
==============

KPActivityView is my own fork from David Sinclair's DejalActivityView. It conveniently displays a horizontal, bezel-style, or keyboard-covering view with a spinning activity indicator and adjustable text. 


Donations
---------

Most of the work was done by David Sinclair. If you would like to donate something, please donate to him: <http://www.dejal.com/developer> 


Requirements
------------

- Xcode 4.2 or later.
- iOS 5 or later.
- ARC.


Features
--------

- **KPActivityView**: a simple horizontal-style loading view, intended for situations where you have a blank view while loading data.
- **KPWhiteActivityView**: the same as the simple one, but with a white indicator and text instead of black, for use in dark views.
- **KPBezelActivityView**: an animated round-rect-enclosed variation, with a gray background covering the parent view.
- **KPKeyboardActivityView**: displays over the keyboard.  Rarely used nowadays (and may be removed in a future version; let me know if you need it).
- A demo project is included.


Usage
-----

Include the DejalActivityView.h and DejalActivityView.m files in your project.

To display the basic `DejalActivityView`, simply use:

	[DejalActivityView showActivityViewForView:self.view];

The activity view is automatically added as a subview of the specified view (e.g. the current content view). No need to save the result to an ivar.

You can instead specify a custom label via:

	[DejalActivityView showActivityViewForView:self.view withLabel:@"Processing..."];

Or specify a custom width, e.g. so you can change the label while it is being displayed without upsetting the geometry, via:

	[DejalActivityView showActivityViewForView:self.view withLabel:@"Connecting..." width:100];

You can also have it manage the network activity indicator in the status bar, e.g.:

	[DejalActivityView activityViewForView:self.view].showNetworkActivityIndicator = YES;

Then when you're done with it, simply invoke this to get rid of it:

	[DejalActivityView removeView];

The other variations are similar.  So for example you can display `DejalBezelActivityView` via:

	[DejalBezelActivityView showActivityViewForView:self.view];

The `[DejalBezelActivityView showActivityViewForView:withLabel:]` and `[DejalBezelActivityView showActivityViewForView:withLabel:width:]` variations are also available.

To remove with animation, call:

	[DejalBezelActivityView removeViewAnimated:YES];


License and Warranty
--------------------

This code uses the standard BSD license.  See the included License.txt file.  

You can use this code at no cost, with attribution.  A non-attribution license is also available, for a fee.

You're welcome to use it in commercial, closed-source, open source, free or any other kind of software, as long as you credit the authors appropriately.

The placement and format of the credit is up to you, but I prefer the credit to be in the software's "About" window or view, if any. Alternatively, you could put the credit in the software's documentation, or on the web page for the product. 

This code comes with no warranty of any kind. 

