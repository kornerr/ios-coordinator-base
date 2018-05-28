
# Overview

This is a sample iOS application to serve as a base for all my sample iOS
applications with Coordinator pattern.

# Preview

This is what the app looks like:

![Preview][preview]

# Architecture overview

* AppDelegate
    * creates UIWindow
    * instantiates SampleCoordinator
    * assigns UIWindow's rootVC to SampleCoordinator's one
* SampleCoordinator
    * instantiates SampleVC and SampleView
    * embeds SampleView into SampleVC
    * displays an alert when SampleView asks to do so
* SampleVC
    * serves as a host for SampleView to display it
    * manages navigation item title property
* SampleView
    * displays content visible from within SampleVC
    * contains button, which only reports the need to display the alert but does not display it

**Note**: Coordinator does actual display of an alert, SampleVC/View do not display anything themselves, this is [SRP][srp] in action.

[preview]: preview.gif
[srp]: https://en.wikipedia.org/wiki/Single_responsibility_principle

