- **Moderator:** Raphael
- **Recorder:** Yanic
- **Date:** 19/03/2025 08:30 - 09:30
- **Location:** Inselspital, Bettenhochhaus, B121
- **Present Persons:** Raphael Keller, Yanic Bernhard, Elisa Stauffer, Silas Kammler, Yassica Umaparan, Jolan Knüsel, Florin Ackermann, Dr. Waldo Valenzuela

# Agenda

## Installation process
Documentation is bad on purpose, so the students need to figure it out themselves.
The problems experienced were mostly related to above, using Windows or misunderstanding of the code. The main branch is good to work with.

## Bugs
While uploading of some DICOM files the slices stay black. Waldo suspects a problem with reading of the contrast value and will look into this bug.

## Testing concept
Unit testing can be done with the python functions. The frontend can be stress tested, cross platform/browser etc. Frontend tests are mostly done manually.
Waldo does not have any testing requirements.

## Documentation / User Manual
Waldo would be interested in a workflow of the frontend. [example](https://vtk.org/doc/nightly/html/classsvtkAbstractCellArray.html)

## Deep Dive Stories
Understand the painting part and modify the palett with other colors. [example](https://kitware.github.io/vtk-js/examples/ResliceCursorWidget.html)

## Explanations of the code from Waldo
- **database** is only to run it locally. The system consists of frontend and backend.
- **docker** runs two isolated cotainers from the rest of the system. local_viewer_phpmyadmin and local_viewer_mysql are exposed to the outside via ports 9099 and 3307 respectively.
- **phpymadmin** depends on mysql. So mysql is run first by docker-compose. The database is empty in the beginning.
- **backend** backend\package.json the bakend is started via "node src/index.js"
- **REST API** and **Graph QL** are used for backend communication. Graph QL has only one endpoint. has a schema (header) and resolver (implementation of functions) section. REST API needs one endpoint per call.
- **sequelize** is a node module that handles database communication.
- **react** it is done class-oriented. There are only a few hook functions
- **debugging** For frontend problems, open Console in web browser and see the calls to backend.
For backend problems, every thing is logged to console.

## read ups according to Waldo
- Node.JS
- Graph QL
- REST API

## next meeting
- 02.04.2025 08:30 B121
- For the next meeting we need to come better prepared. E.g. (We did this, this, followed the code here and then had this issue.)

