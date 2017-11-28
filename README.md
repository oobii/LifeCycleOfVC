# LifeCycleOfVC
Life Cycle of View Controller

Some units of work may only be performed one time—for example, updating a label's font, text, or color. For those tasks, <b>viewDidLoad()</b> is the most appropriate place to do it.

For work that will be performed multiple times, your app can rely on view event notifications. When the visibility of its views changes, a view controller will automatically call its life cycle methods—allowing you to respond to the change in view state.

These methods include:<br>
<b>viewWillAppear(_:)</b><br>
This is called right before the view appears on the screen. This is an excellent place to add work that needs to be performed before the view is displayed (and every time it's displayed) to the user. For example, if your view displays information relative to the user's location, you may want to request the location in viewWillAppear. That way, the view can be updated to take advantage of the new location. Other tasks include: starting network requests, refreshing or updating views (such as the status bar, navigation bar, or table views), and adjusting to new screen orientations.
<br>


<b>viewDidAppear(_:)</b><br>
If your work needs to be performed each time the view appears—but may require more than a couple of seconds—you'll want to place it in viewDidAppear. This way, your view will display quickly as your function continues to execute.
Use the viewDidAppear(_:) method for starting an animation or for other <b>long-running code</b>, such as fetching data.
<br>

<b>viewWillDisappear(_:)</b><br>
s called before the view disappears from the screen. This method executes when the user navigates away from the screen by tapping the back button, switching tabs, or presenting or dismissing a modal screen. You can use the viewWillDisappear(_:) method for saving edits, hiding the keyboard, or canceling network requests.
<br>

<b>viewDidDisappear(_:)</b><br><br>
is called after the view disappears from the screen—typically after the user has navigated to a new view. If this method executes, it is certain the view has disappeared. As such, this method gives you an opportunity to stop services related to the view, for example, playing audio or removing notification observers.
<br>

Call the surepclass version of the methods, i.e.<br>
<b>super.viewDidLoad()</b><br>

In the example for your view to disappear, you'll need to add a second view controller. Otherwise, there'd be no way to navigate from the current view.<br>

The view controller won't load its view until the view needs to be displayed to the user.<br>
Running the app:<br>
First VC - viewDidLoad<br>
First VC - viewWillAppear<br>
First VC - viewDidAppear<br>
<br>
After clicking on the "Second" Tab Button to display second view controller:<br>
Second VC - viewDidLoad<br>
Second VC - viewWillAppear<br>
First VC - viewWillDisappear<br>
First VC - viewDidDisappear<br>
Second VC - viewDidAppear<br>




