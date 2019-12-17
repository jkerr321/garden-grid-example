
Andrew's Garden
==========
A UI for plotting garden plant info on a planting grid and storing that data in a google sheet.

Table of Contents
-----------------

 - [Why](#why-does-this-exist)
 - [Requirements](#requirements)
 - [Usage](#usage)
 - [Development](#Development)
 - [Things still to do](#things-still-to-do)

Why does this exist
------------
Christmas present for my husband 2019!

Requirements
------------

To create a smiliar UI from your own data you will need:
 - a Google sheet containing your data. Mine has the following headings - 
    - POSITION [required]
    - LATIN NAME
    - COMMON NAME
    - PERENNIAL ANNUAL
    - PLANTED DATE
    - COLOUR
    - IMAGE
    - LINK
    - NOTES
    - FILLED [required]
 - A google project connected to your sheet (I used [this very helpful Twilio tutorial](https://www.youtube.com/watch?v=UGN6EUi4Yio) )
 - Your google project credentials saved as environment variables

Usage
-----
via the browser: https://www.andrewsgarden.co.uk

Development
-----

To run locally:

 - Clone the repo to your machine
 - Do $ `npm install`
 - Create a .env file with your google config variables
- Update `renderLandingPage.js` to point to your google sheet: `new GoogleSpreadsheet('[MY_SHEET_ID]')`
- run locally with `$ nodemon app.js`

Things still to do
---------------------

- update back end to be more like dads db - esp init func
- From - Actually fill notes section with notes
- Password for edit mode?
- add older gallery
- get off hobby Dyno
- improve responsive gallery
- linting

**Warnings that might need dealing with:**

A cookie associated with a cross-site resource at http://rhs.org.uk/ was set without the `SameSite` attribute. A future release of Chrome will only deliver cookies with cross-site requests if they are set with `SameSite=None` and `Secure`. You can review cookies in developer tools under Application>Storage>Cookies and see more details at https://www.chromestatus.com/feature/5088147346030592 and https://www.chromestatus.com/feature/5633521622188032.


The connection used to load resources from https://apps.rhs.org.uk used TLS 1.0 or TLS 1.1, which are deprecated and will be disabled in the future. Once disabled, users will be prevented from loading these resources. The server should enable TLS 1.2 or later. See https://www.chromestatus.com/feature/5654791610957824 for more information.