# Developer-Notes

# UIView Controller LifeCycle

# loadView
  - It is only called when the view controller is created programmatically. This makes it a good place to create your views in code.

# viewDidLoad
  - The viewDidLoad event is only called when the view is created and loaded into memory. But the bounds for the view are not defined yet. This is a good place to initialize the objects that the view controller is going to use.
  - Called only once, before viewDidAppear and after viewWillAppear
  - Called when you create the class and load from xib. Great for initial setup and one-time-only work.
  
# viewWillAppear
  - This event notifies the view controller whenever the view appears on the screen. In this step the view has bounds that are defined but the orientation is not set.
  - Called right before your view appears, good for hiding/showing fields or any operations that you want to happen every time before the view is visible. Because you might be going back and forth between views, this will be called every time your view is about to appear on the screen.
  
# viewWillLayoutSubviews
  - This is the first step in the lifecycle where the bounds are finalized. If you are not using constraints or Auto Layout you probably want to update the subviews here.
  -
  
# viewDidLayoutSubviews
  - This event notifies the view controller that the subviews have been setup. It is a good place to make any changes to the subviews after they have been set.
  
# viewDidAppear
  - The viewDidAppear event fires after the view is presented on the screen.A good place to get data from a backend service or database.
  - Called after the view appears - great place to start an animations or the loading of external data from an API.
