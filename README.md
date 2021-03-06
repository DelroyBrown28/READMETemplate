# <div align="center">oneHourmaid</div>

Explanation of what the project is and does

## User Experience (UX)

The point of the project. What the user should and will achieve

* ### Design
    * ###### Imagery
        XXXXX
    * ###### Typography
        XXXXX
    * ###### Colour Scheme
        XXXXX

* ### Wireframes
    XXXXX

### Features
* #### [Main Page Features](https://onehourmaid-project.herokuapp.com/index)
   XXXXX

#### Future Features
XXXXX
___

* #### [Services Page Features](https://onehourmaid-project.herokuapp.com/services)
  XXXXX

#### Future Features
XXXXX
___

* #### [Basic Clean Page Features](https://onehourmaid-project.herokuapp.com/basic_clean_info)
  XXXXX

#### Future Features
XXXXX
___

* #### [Deep Clean Page Features](https://onehourmaid-project.herokuapp.com/deep_clean_info)
  XXXXX

#### Future Features
XXXXX
___

* #### [Cleaner Account Page Features](https://onehourmaid-project.herokuapp.com/cleaner_account)
  XXXXX

#### Future Features
XXXXX
___

### <div align="center">Libraries & Frameworks</div>


##### MaterializeCSS
XXXXX

##### Python/Django
XXXXX
___

### <div align="center">Testing & Bugs</div>

I used both [W3C Validator](https://jigsaw.w3.org/css-validator/) and [W3C Mark Up Validation](https://validator.w3.org/) to ensure the validity of he HTML and CSS code.

**Client Side Testing:**

*--- I would like to simply post a job request for a cleaner to view and contact me accordingly.*
The main page clearly indicates where to go to make a request to a cleaner. Buttons on the page indicate how to go back page if necessary<br>
  

*--- I would like a choice in the level of cleaning service I get.*
After clicking "Request a cleaner" on the main page you have a choice of either a Basic Clean or Deep Clean.<br>

*--- I would like to have the freedom of telling the cleaner exactly what I want instead of just clicking choices.*
Both the Basic Clean form and Deep clean form include a textbox area for the user to verbalize exactly what they want.

*--- I would like the ability to edit or delete a request.*
When the form is submitted, a page with the entered details along with an Edit and Delete button will appear, giving the user the ability to edit or delete a request.


*--- I would like to be informed by email that my request went through to the cleaner.*
An automated email will be sent to the valid email address entered in the email field.

*--- I would like to the ability to see past job requests made by other users.*
All posted jobs are saved in the "Cleaner Account" section which can be accessed from the main page.

**Testing Page Elements:**

**1. Main Page:**
- Both main cards (Request Cleaner & Cleaner Account) go to their respective links **/** *Originally, there was both a sign in and register page available to separate the Customers from the Cleaners. You could register as either a cleaner or a User looking for a cleaner, the customers request would then go to the cleaners account and the communication went from there. I was told to remove this for project purposes as a sign in and register function was not necessary for this project*.
- When checking responsiveness, cards go from being displayed in a row to displayed in a column.
- Hovering over an image reveals the alt text

**2. Services Page:**
- Both main cards go to their respective links.
- Cards show definition of the available service.
- When checking responsiveness, cards turn into a carousel when viewing on iPad or mobile devices.
- Services are still clickable when in carousel mode **/** *I had issues with clicking on cards in carousel mode. Fixed by putting a higher Z-Index on the div element.*
- Bottom buttons, when in carousel mode, are clickable and cycle through the service options **/** *The carousel originally scrolled infinitely, this was fixed by simply adding ```infinite: false,``` to the Slick.JS code.*

**3. Basic Clean Page:**
- Clicking on a form field allows user to enter information accordingly
- If an input field is left empty a red bottom border appears to indicate that the field must be completed. The field should turn green when input is valid.
- The "Contact Number" field only accepts numerical values
- The "Click to pick date" field opens a calender provided by [Materializecss](https://materializecss.com/)
- Calender should not display any past dates **/** *This was fixed by defining the ```defaultDate: "+1w",``` and ```minDate: dateToday,``` in the materialize calender code.*
- The "Valid Email Address" field will only accept a Valid email
- Cleaning request box expands when text exceeds a certain limit.
- When submitting the form you receive an option to Edit, Delete or Exit.
- When submitting the form you receive an automated email to the valid email address entered confirming your request. **/** *The email originally would not send out due to a bunch of different issues with Gmail Security. This was fixed by creating a brand new account and app password to send the automated emails from.*
- Have the ability to edit and re-post a request or delete entirely.
- Back button takes you back a page instead of back to index page.

**4. Deep Clean Page:**
- There are choices to select for a Deep Clean that get saved and displayed in the cleaner account **/** *I can't figure out,at the moment, how to ignore returning ```null``` values from MongoDB*
- As with the Basic Clean page, the submitted form will trigger a choice of Edit, Delete or Home, whilst also displaying the users input information. **/** *originally the Deep Clean form would not trigger the auto email. I fixed this by writing separate code to send the Basic Clean form and the Deep Clean form. This ended up being useful as now i get separate Basic Clean and Deep Clean requests instead of all requests in one*.
- Have the ability to edit or and re-post a request, or delete it entirely.

**5. Editing a Request:**
- User is able to edit the request made by going back to the form and re-filling the necessary information
- The updated information is then able to be viewed in the Cleaner Account.
  
**5. Deleting a Request:**
- User is able to delete a request before it is posted to the Cleaner Account

**5. Cleaner Account Page:**
- All jobs save for future reference
- User has the ability to view requests and mark jobs as complete.**/** *Originally, the user had the ability to chat directly with the Cleaner using ghe SocketIO plugin. I was told to remove this as it was too much for project purposes.*
- Pop up appears letting the user know they've marked the job as done.
___

### <div align="center">Future Project Implementations</div>

XXXXX
___


### <div align="center">Deployment</div>
The project was developed using [Visual Studio Code](https://code.visualstudio.com/) then pushed to [Github](https://github.com/) and [Heroku](https://dashboard.heroku.com/apps/onehourmaid-project) using the git CLI

When deploying this project to Github, i took the following steps:
1. Create a new Github Repository.
2. Create a repository name.
3. Copy/paste the following Command Line commands to create a repository in the CLI.
```
echo "# testing123" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/DelroyBrown28/testing123.git
git push -u origin main
                
``` 
4. Push code to Github using ```git add -A``` then ```git commit -m "Commit message here"``` and finally ```git push```
5. Once the code is up on Github, go to settings, scroll down to "Github Pages" and change "source" to "master".<br>
<img src="static\README_files\githubpages.PNG" style="height: 200px; border: 2px solid black;"><br><br>
6. Refresh after a minute or so and a green banner displaying the URL for the deployed site will be visible.<img src="static\README_files\greenbanner.PNG">

When deploying to Heroku, I took the following steps:
1. Create a new Heroku app.
2. Go to the "Deploy" tab and connect to Github.<img src="static\README_files\deploy.PNG">
3. Once connected to the correct Github repository, make sure all code is pushed to github using ```git add -A``` then ```git commit -m "Commit message here"``` then ```git push``` and finally ```git push heroku master```
4. Once pushed to heroku, click the link in the terminal and the deployed project appears.<br><br>

**Running Project Locally:**

You can clone this project from Github by following these steps:
1. Visit the [Github repository](https://github.com/DelroyBrown28/oneHourmaid_cleaner).
2. At the top click the dropdown labelled "Code".<img src="static\README_files\clone.PNG">
3. Copy/paste the HTTPS URL
4. In the terminal type ```git clone https://github.com/DelroyBrown28/oneHourmaid_cleaner.git```
5. Hit enter and the repository will be cloned to your machine.

You can run the app by simply following this link on Heroku to [oneHourmaid](https://onehourmaid-project.herokuapp.com/)<br><br>

### <div align="center">Credits</div>

##### Media:
XXXXX

##### Code:
- [MaterializeCSS](https://materializecss.com/) was used to implement all forms in the project.
- [Slick](https://kenwheeler.github.io/slick/) was used to build the carousel on the Services page when in mobile view
- [JQuery](https://jquery.com/) is used to help handle the functionality of the calender and any confirmation messages.