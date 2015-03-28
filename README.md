# radial-menu-widget
Automatically exported from code.google.com/p/radial-menu-widget

Getting started with radial widget. Updated Jun 19, 2012 by strider2023
Introduction
Use the following to get started with radial menu widget. Radial widget can be used over normal menus in android as it is visually more appealing and has a better UI experience.

Features
Fully customizable in terms of background color, text size and color, icon scaling, widget size and positioning on the screen.
Easy implementation.
Usage
To use radial menu in your andorid application, download the library file form the downloads page and place in the libs folder (create one if it doesnt exsists) of your project.

In your class file add make a new object of the radial menu widget and menu item.
RadialMenuWidget pieMenu; RadialMenuItem menuItem;
Init the objects
pieMenu = new RadialMenuWidget(this); menuItem = new RadialMenuItem("Test","Test");
Add it to the widget using
pieMenu.addMenuEntry(menuItem);
Use pieMenu.show(v); to display the menu and pieMenu.dismiss(); to remove menu.
Note: The widget will automatillay remove itself if toch is detected outside of the drawing area.

Comment by minsche...@googlemail.com, Sep 6, 2012
Hi, I declared the following but wouldn't work and crashes:

import com.widget.radialmenu.RadialMenuItem?; import com.widget.radialmenu.RadialMenuWidget?;

import android.os.Bundle; import android.view.View;

public class ScrollWheelActivity? extends AbstractActivity? {

RadialMenuWidget? pieMenu; RadialMenuItem? menuItem; View v;
@Override protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState); pieMenu = new RadialMenuWidget?(this); menuItem = new RadialMenuItem?("Test","Test"); pieMenu.addMenuEntry(menuItem); pieMenu.show(v);
}
@Override protected void onStop() {
super.onStop(); pieMenu.dismiss();
}
}

Any idea?

Regards

Sebastian

Comment by minsche...@googlemail.com, Sep 6, 2012
Sorry about the question mark that got automatically generated, not sure how to get rid of it.

Comment by minsche...@googlemail.com, Sep 6, 2012
Ok I got the example working, but how would you make it rotatable, much like an actual iPod UI? Thanks

Comment by qadir....@gmail.com, Apr 23, 2013
How to Open Radial-Menu-Widget in onCreate instead of on Button Click event thanks

Comment by project member strider2023, Apr 25, 2013
It can only be done with the v1 version.

Try this piece of code in onResume...

findViewById(R.id.alt_fragment_container).post(new Runnable() {

public void run() {
pieMenu.show(findViewById(R.id.alt_fragment_container));
}
});
Comment by sonia...@gmail.com, May 7, 2013
Hi!

There's a specific way to understand how to implement this into an Android project?

Thank you so much!

Comment by bramara....@gmail.com, Aug 13, 2013
how can i write intent to each sub menu item for navigation

Comment by bramara....@gmail.com, Aug 13, 2013
how can i write intent to each sub menu item for navigation

Comment by victor.e...@gmail.com, Sep 9, 2013
Hi! When you rotate the device or if you increase the size of the inner circle in version 1 example, you get the circle cut by one side, im thinking in maybe the drawing limits, but i cannot find a way to increase them. Anyone here with the same issue?

Comment by 1HabeebA...@gmail.com, Dec 2, 2013
Hello, how would I go about having this show by default?

Comment by nagarmin...@gmail.com, Jan 27, 2014
help me! cannot write intent in menus.

Comment by amr.fais...@gmail.com, Feb 11, 2014
Hello guys. I'm wondering how can i center the "Pie" menu inside a View? Thanks

Comment by gowrisha...@gmail.com, Feb 25, 2014
Hi., I need this type of radial menu. I need it in center of the page. Can anyone please tell me about the complete project structure? and which jar file we need to use for getting it?

Thanks

Comment by chenai.x...@gmail.com, Feb 28, 2014
Hi, for the radial menu is there any method can change the menus size?

Comment by coolboyk...@gmail.com, May 20, 2014
how to increase menu size and how i can set drawable to menu background?
