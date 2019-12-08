# Squirrel Sightings Web Application 

This file is written to summarize the tools and functions of this web application, which is intended to track and visualize all squirrel sightings in Central Park. 

## Main Functions
This Django-based Web Application tracks all recorded squirrel sightings in Central Park, with all dataset retrieved from the [2018 Central Park Squirrel Census](https://data.cityofnewyork.us/Environment/2018-Central-Park-Squirrel-Census-Squirrel-Data/vfnx-vebw)

Users of this web application can add, edit, and delete sightings, as well as obtain some key statistics regarding the sightings. Additionally, the map displays the geographical location of the sightings.

## Installation
Clone this repository into your project with the following SSH:

```
put ssh here
```

### Installation of Dependencies
If a requirements.txt file is expected in the root of projects, install the production requirements with this code on the command line:

```
$ pip install -r requirements.txt
```

## Management Commands
These commands allow you to import and export the dataset:

> **Import**: A command that can be used to import the data from the 2018 census file in CSV format

```bash
$ python manage.py import_squirrel_data /path/to/file.csv
```

> **Export**: A command that can be used to export the data from the webapplication in CSV format

```bash
$ python manage.py export_squirrel_data /path/to/file.csv
```

## Features

When running the server in your browser, adding different views location to the url leads you to different API with specific functions

> **Sightings**
* **Function:** Sightings lists all squirrel sightings with links to add, edit and delete sightings
* **Location:** /sightings

> **Map**
* **Function:** Map displays the geographical locations of all recorded sightings
* **Location:** /map

> **Add**
* **Function:** Add allows you to save a new sighting into the database. Specific fields include: Latitude, Longitude, Unique Squirrel ID, Shift, Date, Age, Primary Fur Color, Location, Specific Location, Running, Chasing, Climbing, Eating, Foraging, Other Activities, Kuks, Quaas, Moans, Tail flags, Tail twitches, Approaches, Indifferent and Runs From.
* **Location:** /sightings/add

> **Update**
* **Function:** Update the information about a particular sighting by referencing the unique squirrel ID 
* **Location:** /sightings/<unique-squirrel-ID>
  
> **Delete**
* **Function:** Delete a particular sighting by referencing the unique squirrel ID
* **Location:** /sightings/<unique-squirrel-ID>
  
> **Statistics**
* **Function:** Statistics list several general information about the recorded squirrel sightings
* **Locations:** /sightings/stats

## Additional Notes

* The map might require more time to load larger datasets
* When a new sighting is added, if the Unique Squirrel ID is already in use, the web application does not add this 'new' sighting into the database

## Issues Tracker

Please submit pull requests on GitHub <git@github.com:shinler/I_Saw_A_Squirrel.git> if you spot any issues with our code

## Contributors
**Group Number:** Project Group 49 Section 2
**Group Members:** Douglas Chan (uni sc4619), Shin Ler Low (uni sl4617)

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
