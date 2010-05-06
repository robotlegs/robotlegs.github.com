---
layout: post
title: HBO PunchZone - Robotlegs for the Unanimous Decision
categories:
- community
- success-story
---
From James O'Reilly:

Choosing the Robotlegs MVCS framework for developing [HBO Boxing’s PunchZone microsite](http://hbopunchzone.com) was a unanimous decision based on a heavy hitting combo of quick development, memory management, and flexibility.

Right hook…  Robotlegs enabled us to build our application very quickly because we spent most of our time writing the application rather than writing code required to use a framework.  My favorite feature of Robotlegs is its use of dependency injection to create a very loosely coupled application.  I found this to be a tremendous time saver because dependency injection in Robotlegs is all handled under the hood through mappings I define.  By avoiding the object instantiation life cycle headache, I am able to stay focused on writing application logic instead of being distracted with chicken-and-egg-like brainteasers.  In addition, the loosely coupled classes really helps simplify unit testing.  Running test suites regularly can help reduce time wasted hunting down difficult to reproduce anomalies.

Uppercut…  Memory management of the key players such as models, views, mediators and commands are all handled very well right out of the box.  There is no need for me to spend time writing cleanup code for objects created or mapped by the framework.  For example, all framework event listeners I map inside a mediator are automatically cleaned up when the mediator is destroyed.  In turn, that mediator is automatically destroyed when the view it’s mediating is destroyed.  This automatic cleanup reduces the profiling effort to just that of the business logic.

Body blow…  Like any project, requirements change.  It is always important that we develop applications that can evolve over time.  Thanks to the organized structure of a Robotlegs MVCS implementation we have a very flexible application that can be modified with little to no impact on the rest of the application.  Do we need the app to do something new?  No problem, we probably just need to drop in a new command or two.  Do we need the app to visually display data differently?  In that case we probably just need to modify a view.  Its encapsulation and loosely coupled classes that really help cut down time when changing an application’s feature set.