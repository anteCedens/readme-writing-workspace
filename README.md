# **Ecommerce Site Project**


This project was built for the purposes of one of my personal projects ("milestone projects") at Code Institute.

This was a Django full stack project, to achive the following:

>Build a Django project backend by a relational database to create a website that allows users to store and manipulate data records about a particular domain.

Or, slightly more specifically:

>- build a full-stack site based around business logic used to control a centrally-owned dataset
>- set up an authentication mechanism and provide paid access to the site's data and/or other activities based on the dataset, such as the purchase of a product/service

Two other important points were:
- using a relational database (recommending MySQL or Postgres)
- using Stripe payments (naturally using Stripe's test functionality, rather than actual live payments)

The project is built on the basis of and following the tutorial project shown as a part of the course, the main differences 
being the "subject", so to speak - I chose to try and do an online bookstore; and my attempt at using Bulma (the tutorial uses Bootstrap).

---

## Table of Contents
1. [**Design and Features**](#design-and-features)
    - [**Project Purpose**](#project-purpose)
    - [**Design**](#design)
        - [**_Fonts_**](#fonts)
        - [**_Images and Colors_**](#images-and-colors)
        - [**_Navigation_**](#navigation)
        - [**_Responsive Design_**](#responsive-design)
    - [**Features**](#features)
2. [**Technologies Used**](#technologies-used)
3. [**Testing and Features Left to Implement**](#testing-and-features-left-to-implement)
    - [**Testing**](#testing)
        - [**Deployment**](#deployment)
            - [**Local Deployment**](#local-deployment)
            - [**Remote Deployment**](#remote-deployment)
    - [**Features Left to Implement**](#features-left-to-implement)
4. [**Credits**](#credits)
    - [**Content**](#content)
    - [**Media**](#media)
    - [**Acknowledgements**](#acknowledgements)

---

## **Design and Features**

### **Project Purpose**

In addition to what was already mentioned above - in a nutshell: building an ecommerce site
using Django, further focus and emphasis is to be placed on

- a multiple apps structure
    - to be composed of multiple apps, each ideally reusable (an app for each potentially reusable component of the project))

- user authentication & interaction
    - include an authentication mechanism allowing a user to register and log in (plus some motivation - i.e. a reason - fo a user to do so)
    - include at least one form with validation that will enable users to create to interact with the site (edit models in the backend)
In other words:

>create functionality for users to create, locate, display, edit and delete records

and also hopefully do that in a both visually appealing and user friendly manner (ease of use).


### **Design**

#### **_Fonts_**

Site uses two fonts:
 - `Caveat Brush`
 - `Dekko`

 They're chosen as a pair because they work well together, and guided by the general idea to make the site more unassuming and
 less "business-y", with more of like a playful, informal, friedlier note.
 General guiding idea was to use `Dekko` as a font that would increase readability, when compared to `Caveat Brush`: although the
 latter seems more "interesting" and "fun", some of its variants - like its bold rendition with an increased font size - might hinder
 readability.
 So, for instance, `Dekko` might be used for something as a product's (i.e. book's) title; while `Caveat Brush` "looks more interesting" on a navbar.


#### **_Images and Colors_**

 There is basically only two images used that are not products images themselves: the background and the logo.
 Following what is described about the fonts, imagery used tries to follow suite in being less "stern". 

 Colors used as mainly black and white - or rather a "black-looking" specific shade of grey, taken from Bulma's documentation,
 called "Grey dark" there. "Bulma Grey dark" is used to also match some of Bulma's tooltips used. There are also some "neon" effects added to the white color, for instance when howering over certain `<a>` elements.
 Those colors are chosen to be "simple", work well together while having a high-contrast relation between themselves, and also work
 well with the background. 

 There's a favicon implemented as well - the same one as is used for the site's logo.

#### **_Navigation_**

Navbar consist of a site title/logo, which also functions as a home button, and three other elements: a search bar, a view bag button, 
and a log-in (sign-up or sign-in) button.

There are some animations inplemented, to hopefully help the user better understand what's going on. The view bag button has
a items counter - which displays the total number of items it the bag. That counter works in connection with the add-to-bag button
on the product detail page(s): add-to-bag button has a little "+" icon, that when the button is clicked, "jumps" into the bag, thus
signaling to the user the additon when succesfully performed, and also directing attention to the bag items counter, which has now incremented.

The home/index page also has animation that is triggered when the user hovers over "Browse The Books!" button: a beating heart appears under that button.
The idea is something along the lines of "books make our hearts beat"; or "our heart beats for books"; or, simply, "we love books", we love browsing through
books, we love buying books, etc. The heart animation is also my sort of a tribute to https://www.freecodecamp.org/, which I love.

There is also a back-to-top button that appears on the products page when a user scrolls down past a certain point.

#### **_Responsive Design_**

The project basically is built using Bulma, and it tries to utilize Bulma's responsive design ideas and structures.
A few words here also on why Bulma is chosen: mainly, the tutorial project uses Bootstrap, and I wanted to try and step always
and set myself apart from that and use a different CSS framework; I never used Bulma before, and I wanted to try it.

(Although, not using Bootstrap in this particular instance had its own caveats, namely in regards to "crispy forms", buta bit more on that below.)

Main feature on smaller screen, basically, as opposed to the desktop view, is that the navbar condenses into a hamburger menu:
the logo/home button always remains visible, while the rest of the navbar's elements become contained in the hamburger menu.


## **Technologies Used**

- **_IDE and code storage_**
    - GitPod - used as the online IDE
    - GitHub - for the storage of the code online

- **_Full-stack framework_**
    - Django
        - list of installs is in requirements.txt

- **_Database_**
    - Postgres when deployed
    - Django's db.sqlite3 during development

- **_Front-End_**
    - HTML
    - CSS
        - Font Awesome
        - Google Fonts
        - Chrome DevTools
    - JavaScript
        - jQuery

- **_Deployment_**
    - Heroku
    - AWS

## **Testing and Features Left to Implement**

### **Testing**

Apart from manual testing as the project was buing built:

- [HTML Validator](https://validator.w3.org/)
- [CSS Validator](https://jigsaw.w3.org/css-validator/)
- [JSHint](https://jshint.com/)
- [PEP8](http://pep8online.com/)

The project is unfinished: Stripe integration plus notification emails setup needs finishing, as well as the Profiles app bit, and the CRUD functionality
for superusers.

There are still some residual Bulma-inherited stylings for certain pesudo-states on certain elements.

The tutorial project makes use of "crispy-forms" in connection with Bootstrap. I tried using the Bulma equivalent, but, as
it clearly warned here 

>This project is an early work in progress. You should not use this package yet, as it is poorly documented and is missing many important features

and the use of them causes more issues than the gain is. But, on the other hand, if Bootstrap is used - whose crispy-forms work fine - then there are
some clashes between Bootstrap and Bulma in the code.

So, to continue to use Bulma, the project does not use crispy-forms.

#### **_Deployment_**

##### **_Local Deployment_**


In order to run this project locally, you will need to install: 
- An IDE of your choice (VS Code, etc.)
- [Python3](https://www.python.org/downloads/)
- [PIP](https://pip.pypa.io/en/stable/installing/) - to install the app's requirements (listed in the "requirements.txt")
- [GIT](https://www.atlassian.com/git/tutorials/install-git) - for version control
- [MongoDB](https://www.mongodb.com/) - to work with the database


After this is installed, download the .ZIP file of the repository, unzip this file, and then:

- in the CLI with GIT installed, enter the following command: 
   
        https://github.com/anteCedens/CI-MS3-cookbook.git

- navigate to the to path using the `cd` command. 
- create an `env` file with your credentials (values)
- install all of the app's requirements for running, listed in the requirements.txt file, by using the following command:
    
        sudo -H pip3 -r requirements.txt

- sign up for a free account on [MongoDB Atlas](https://www.mongodb.com/) and create a new database called "ci_ms3_cookbook". Name of the database collection 
can be seen here: [MongoDB collection schema](wireframes/MS3_MongoDB_schema.JPG). 
- now you should then be able to launch your app using the following command in your terminal:

        python3 app.py

##### **_Remote Deployment_**

To remotely run this project: 

- in your GitPod workspace, create a `requirements.txt` file using this command in the terminal: `pi3p freeze > requirements.txt`.
- create a `Procfile` using this command in the terminal: `echo web: python app.py > Procfile`.
- `git add` and `git commit` the new requirements and Procfile and then `git push` the project to GitHub.
- go to [Heroku](https://dashboard.heroku.com/login)
- click the "new" button, give the project a name & set the region to Europe. 
- from the Heroku dashboard of your newly created application, click on "Deploy" > "Deployment method" and select GitHub.
- confirm the linking of the heroku app to the correct GitHub repository.
- in the Heroku dashboard for the application, click on "Settings" > "Reveal Config Vars".
- set the config variables as so:

| KEY | VALUE |
--- | --- | 
IP | 0.0.0.0|
PORT | 8080|
MONGO_DBNAME | <database_name>
MONGO_URI| mongodb+srv:// \<username>: \<password>@<cluster_name>.mongodb.net/<database_name>?retryWrites=true&w=majority 

- in the Heroku dashboard, click "Deploy"
- the application should now be deployed

### **Features Left to Implement**

**_Carousel "randomizer"_**

Currently, the carousel and the index page displays all the images from the database, 
in the sequence in which they are stored in the database, which is chronologically. And the 
sequence resets - i.e. starts from the beginning - each time the index page is loaded.

So, if an image stored in the database last, it would go to the back of the carousel, and get displayed last. 
It's a FIFO principle, basically (**F**irst **I**n **F**irst **O**ut - i.e. what is stored in the database 
first, is displayed out in the carousel first also).

With a larger number of entries, some of the images would in practice never get displayed, or more precicely, 
they would never get _seen_, as it could be not expected for a user to stay on the index page long enough for those 
particulary images to be displayed on the carousel.

Or, in other words, some of the images would not "get a fair chance to be seen". And the idea, or the desire, is that all 
images, which represent recipes, get treated equally in that regard.

I attempted to change the "step" option of the carousel - i.e. parameter which controls the image display pattern: default "step" is 1, 
which means the carousel displays the next image in the que. So if the "step" is set to, for instance, 3, the carousel would display every 
third image. But, that doesn't visually look right, becuase the transition to the following image doesn't render seamlessly, but it rather 
looks like the carousel is spinning at great speed until it reaches the desired image.

So a "carousel randomizer" is an idea where the carousel is set to display images in random sequence, and the sequence is randomized (or "shuffled") 
anew every time the index page is loaded.

**_Delete confirmation_**

Currently the delete button in the Edit Recipe form form is set up that you only press it once, and the recipe is deleted. I'd like to have an additional 
"delete confirmation" feature set up: when the delete button is pressed, a message would pop up (using a Materialize "modal", for instance) asking the user 
to confirm deletion.

**_Character restriciton_**

Currently, there is no character restriction in the forms, when adding a new recipe. Implementing such a feature might be beneficial, namely for such fields in 
the form as the recipe's name, and short description.

Also, additional form validation functionalities are to be considered.

**_Further form styling_**

Maybe make the forms (for adding and editing recipes) more visually appeling, based on user feedback, in regards to typography, or button styling. Possibly adding further data entry fields about the recipes, such 
as serving, ingredients, course (main, side, starter, etc.), or meal (breakfast, lunch, dinner).

**_Search bar_**

Currently there is none.

## **Credits**

### **Content**

Content on the index and About pages was written by me.

Recipes entered in the database at the moment of writting this, were taken from these sources:

- https://tasty.co/recipe/baked-avocado-eggs
- https://www.delish.com/cooking/recipe-ideas/a26728380/baked-pineapple-salmon-recipe/
- https://www.bbcgoodfood.com/recipes/spaghetti-meatballs
- https://www.allrecipes.com/recipe/257198/thin-crust-pizza-dough/
- https://www.bbcgoodfood.com/recipes/chorizo-mozzarella-gnocchi-bake

### **Media**

All recipes images diplayed on the site as of the moment of writting this are rendered via their URL's, so a source 
for the image is always evident.

All the other images used, stored in the project on GitPod, are from:

- https://hipwallpaper.com/
- https://wallpaperaccess.com/

except for the 404 image, which is from:

- https://www.freepik.com/

Icons used are from:

- https://material.io/resources/icons/?style=baseline
- https://fontawesome.com/

### **Acknowledgements**

For the core know-how on how to build a project like this, I've used Code Institutes "Task Manager" 
tutorial project:

- https://github.com/Code-Institute-Solutions/TaskManager

In regards to designing an online cookbook specifically, I've browsed through my fellow students' projects, 
such as:

- https://github.com/sohailshams/cookbook
- https://github.com/sabinemm/recipe-site-ms3
- https://github.com/amybru/byoboba
- https://github.com/Trevbytes/Chickpeas
- https://github.com/ss00831/milestone3
- https://github.com/ajgoward/daddies_recipes_MS3
- https://github.com/lewisclark4/CI-MilestoneProjectThree
- https://github.com/ceciliabinck/cook-with-me

As writing the readme.md goes, for me, since project one, when in doubt or stuck, it's always been W.W.C.L.D.: 
What Would Claire Lally Do?:

- https://github.com/ClaireLally8

Other resources used:

- https://www.lipsum.com/
- https://www.diffchecker.com/diff
- https://jpg2png.com/
- https://convertico.com/