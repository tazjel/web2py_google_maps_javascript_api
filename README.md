# web2py_google_maps_javascript_api
Project to show how to run the Google Maps Javascript API from a plain-vanilla web2py application

The significant impediments to easily inserting a Google map inside a Web2Py view are:

1. The Google maps Javascript API will not render your map unless all of your enclosing divs have a style containing a non-zero height, making your 
2. Web2Py places your view's body inside two nested divs that do not contain the ID attribute, so your map is not rendered.

The solution:
1. Edit layout.py so that in the center column it places ID attributes on the two divs enclosing the center column
2. In your view, assign styles to these same IDs to give them height

The app also demonstrates how to pass the center and zoom from the pure-Python controller to the view displaying the map.
