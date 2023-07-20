# Business Problem
## Project - Radio Station Look-up

There are many FM radio stations that listeners can tune into, but they need to check each clear channel to know what stations are available. Because of this, potential listeners miss out on listening to radio stations or shows they may be interested in. Radio listeners need an easier way to view nearby stations and to discover which stations are broadcasting what sort of shows at certain times. Since different stations may play different genres at different times, listeners should be able to figure out a listening schedule that fits their tastes. Our team will develop an application to remove the guesswork and channel-surfing radio listeners undergo to find the perfect broadcast by creating a database that queries by preferences specified through a GUI.

## High-Level Interface
We will provide a GUI application allowing users to add fields like location, time, or radio broadcast preference to query stations that fit the user-specified preference fields as closely as possible. The resulting queried stations will provide as much information as the user wants, including the frequency, call sign, current radio show, and/or the current host.

# Project Proposal (Revised)

## User Interactions
-	Look up radio stations by frequency or call sign to see scheduled shows, hosts, DJs, and genres.
-	Input current location to find available stations within a broadcasting radius
-	Search scheduled radio show start times
-	See radio shows being broadcasted currently
-	Search for radio shows by genre, host, or broadcast time.
-	Input station preferences (location, schedule, radio show type)
-	Query stations that fit user-specified preferences and display a list of qualifying stations. 

## Customer Page GUI

-	Customers do not need an account to access our radio app. 
-	Customers search for radio shows by categories such as starttime, day of the week, host, genre, station frequency or callsign, or city.
-	Users are presented with  a search field where they can enter a search term as well as a dropdown menu next to the field where they can select the category of the field. This allows users to specify how broad or narrow the search can be by selecting the categories they care about. . 
-	Categories to search by include: show starttime, day of the week, host first name and last name, genre, station callsign(KUOW, KEXP, ect.), station frequency ( 90.3, 88.5, 101.7, ect), or city.
-	Any category that is not specifically selected will be assumed to be a wildcard search, and will return all results within the parameters of other search categories.
-	Additional search fields can be added to search for multiple different categories at the same time. The additional fields can be designated as “and”, “or”, or “not” to further narrow the search. 
-	The result of this search will be a list of shows that fit the selected criteria input by the user.
-	Customers can then sort results ascendingly or descendingly by each category(show name, host, genre, day of the week, time of day, station name or frequency).
-	Customers have the option of further limiting searches by inputting their location as a set of latitude and longitude coordinates.
-	Clicking a button to sort by distance will prompt the user to enter the latitude and longitude of the location they want to search from.
-	Searching by location with no other criteria will show the user a list of all the shows broadcasting from stations that the location is within broadcasting radius of. 
-	If the user instead chose to input further search criteria as described above, the resulting list will be a result of shows filtered by what the user can tune into at their location. 
![schema](https://github.com/chloeNgo99/LSFM/blob/main/img/AdminGui1.png)

## Admin Page GUI
To update or insert data in our database, an administrator must enable administrator mode from the start menu using a password. To update a record, the same search function will be used to find a record that needs to be updated. To insert a new record, a new window will appear where the admin can fill out the new record and the app will execute the corresponding CRUD command.

-	From LSTN.FM’s start window, there will be a button on the bottom right labeled “enable administrator mode”. When clicked, a prompt will appear asking for a password. When the correct password is entered, the enable admin button will be replaced by an add record button
-	To change a record, like what genre a radio show is, the admin can look for the show they want to change, and the results page will have an edit button next to each record.
-	Clicking edit will make a new window appear where each field for that show is in an editable text box. The admin can make changes from there and commit changes or discard them by clicking commit or cancel respectively.
-	To add a new record, the admin can click the add record button from the start screen and a window similar to the editing window will appear. This window will have a drop-down menu at the top to indicate which table will be updated with this new record, and editable text fields for each of that table's columns. 
-	If that record needs to relate to another record, like a show to a station, the admin can use the search function to find that record and add in attributes of that record.
![schema](https://github.com/chloeNgo99/LSFM/blob/main/img/AdminGui2.png)

# Schema
![schema](https://github.com/chloeNgo99/LSFM/blob/main/img/LSFM%20Schema.png)

# Development tools and Environment.
For development tools, we agree on using the Appsmith framework to build the radio station GUI:
-	We’ll use Postgres to create our own Radio Station database according to the schema.
-	Next, we will connect our database by using appsmith frameworks which are primarily run by Javascript.
-	We’ll be using Docker, which is provided by appsmith, to create an installation folder that holds our database for local hosting.
-	The Appsmith tool itself provides GUI creation tools. 

DATABASE SOFTWARE: Postgres
UI TOOLS: Appsmith, Javascript

HOSTING AND ACCESS: Local hosting with Docker as an interface for Appsmith




