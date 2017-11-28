# LifeCycleOfVC
Life Cycle of View Controller

Some units of work may only be performed one time—for example, updating a label's font, text, or color. For those tasks, <b>viewDidLoad()</b> is the most appropriate place to do it.

For work that will be performed multiple times, your app can rely on view event notifications. When the visibility of its views changes, a view controller will automatically call its life cycle methods—allowing you to respond to the change in view state.

These methods include:<br>
<b>viewWillAppear(_:)</b><br>
<b>viewDidAppear(_:)</b><br>
<b>viewWillDisappear(_:)</b><br>
<b>viewDidDisappear(_:)</b><br><br>

Call the surepclass version of the methods<br>
<b>super.viewDidLoad()</b><br>


