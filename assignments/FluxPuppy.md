# About FluxPuppy and potential work to do


**FluxPuppy** is a mobile Android application for use with the LI-840A gas
analyzer. The application can be used to observe, collect, and organize
data streamed from the analyzer into user specified data sets. FluxPuppy
is designed to replace the data collection system implemented by LI-COR,
by providing many features not present in the current system such as
advanced organization, live data readout, and included metadata

The app is part of a large project in our lab that are supported by several National Science Foundation (NSF) grants. In general, our lab receives funding from several federal agencies such as: NASA, NSF, DOE, NEON, and USGS.

Here are the proposed tasks that need to be done:

### Project 1) General cleanup of the source code:
     - Fixing unnecessary public variables and methods to private
     - Addressing android studio suggestions/warnings regarding code cleanup
     - Overall the code is commented, but it would benefit from an
overview to make sure all comments make sense and if anything else needs
proper commenting
     - Inspection of the code for unused variables and methods or
repeated modules
     - overall software engineering cleanup

### Project 2) Documentation
     - The app currently has an outdated user manual and technical
manual. But after recent changes, it requires a review to make sure all
menu and details described well
     - Prepare general UML diagrams for the code

### Project 3) Data mocker for the app
     - The app reads the data from USB and BT ports. It would be nice to
have a data mocker to test the app.
     - Format of the data is super simple. Every half a second, a short
XLM string is sent.

### Project 4) Improvement of the existing app.
     - We are also open to new ideas for modifying the app. I think if a
software engineer looks at a code they may have suggestions on how to
improve the functionality inside the app.


All codes are on my github:
https://github.com/bnasr/FluxPuppy

This is a great opportunity for computer science students who
want to join the industry or even consider to continue to grad school, Bijan would be happy to write recommendation letters for students who work hard and successfully complete the tasks for their future careers/applications.
