# proxyclick_mobile_assessment
This repo will contain the infomation about the proxyclick assessment exercise for mobile candidates.

# Preamble

This exercise is designed to assess your technical level in Xamarin.iOS development and your coding level in general.

Your solution will be evaluated from several perspectives:`

1. Functional: does your solution work?
1. Architectural: does your solution have a good architecture that respects MVVM principles and best practices?
1. Coding: does your solution respect best coding practices and does it follow "clean code" principles?
1. Design: does your solution respect the design requirements ?

When doing this exercise please code as if you were making production ready code.

# Your task

## Overview

Build Xamarin iOS (not Xamarin.Forms) iPad app that logs into a proxyclick account and downloads a list of visits for the day and the list of frequent visitors. 

* A *visit* is defined as a meeting for a specific visitor on a specified date and at a specified time. 
* A *frequent visitor* is defined as a visitor that is recognized by the proxyclick system and that has the permission to visit a location unannounced.

## What you will need.

1. API documentation : https://api.proxyclick.com/v1/docs/#introduction
1. The company ID to be used is the following: CO-CXER585
1. Client ID: 98C5EB84170E6FB3617C47A5B17ECFACB4A0FD49
1. Client secret will be sent via email


## Requirements:

Two screens will need to be devlepped :

### Login screen

1. The login screen has 2 textfields : username and password and a login button.
1. The login button should call the login api endpoint when tapped
1. If login has invalid credentials display appropriate error messages in a popup
1. Credentials and the access token should be stored on disk.
1. If the access token is available when starting the app the login screen can be skipped and the stored access token can be used for API calls
1. If at any time an api call receives a 401 unauthorzied the app should redirect the user to the login screen to refresh their access token.
1. If there is no internet connection then the system needs to check if it has stored credentials and data from a previous download and if that’s the case then it needs to show the list with the saved data if not it needs to display a message and stay on the login screen.

### Vistis and visitors screen

Once logged in the user gets redirected to the screen that displays the list as described below:

1. Download and display visits for the day and frequent visitors in a list with 2 sections : visits and visitors.
1. In the visits section of each cell needs to display the name of the visitor and the start time of the visit. In this section the text color should be green.
1. In the frequent visitor section the cell needs to display visitor's full name. The text color in this section should be blue.
1. If there are no items in a given section display a cell in that section that reads “No items”
1. Display a refrsh button below the list. When this button is tapped the system should redownload the data from the server

1. The list screen has the following design requirements:
  a. the list should take 50% of the screen width
  a. the list should take 70% of the screen height 
  a. The button should be horizontally aligned with the center of the list
  a. The button should be vertically aligned in it’s vertical space (30% of screen height)
  
1. If there is a backend error downloading visit/visitors display an error message in a popup.

# Last notes

1. Don't hesitate to ask questions! Asking questions whatever they may be will not be held against you in your evaluation.
1. If anything is not specified in the above explanation, it is not expected. For example: nothing was mentionned about the specific design of the login screen which means you are free to design it as you want.
1. You are given 3 days to finish this exercise. If this is problem  please don"t hesitate to contact me.
1. You are free to use any external libraries and/or nuget packages you deem useful.

