# ict239-assessment-1-solved
**TO GET THIS SOLUTION VISIT:** [ICT239 Assessment 1 Solved](https://www.ankitcodinghub.com/product/ict239-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121190&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ICT239 Assessment 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
&nbsp;

1. This End-of-Course Assessment paper contains THREE (3) questions and comprises NINE (9) pages (including the cover page).

IMPORTANT NOTE

Please Read This Information before You Start Working on your ECA

Submission

Once you have submitted your ECA assignment, the status is displayed on the computer screen. You will only receive a successful assignment submission message if you had applied for the e-mail notification option.

This paper continues the TMA theme on the development Web Application for viewing and booking of staycation packages.

In TMA Q2, you were asked to follow the MVC framework to design and implement the Web Application. In ECA Q1, you are further asked to follow the Object Oriented Programming principles to implement the Model of MVC through the use of MongoEngine library. Given the following file directory structure:

/home/user/Projects/ECA └─ app

├── assets/

│ ├── css/ # directory with css files

│ ├── img/ # directory with image files

│ └── js/ # directory with JavaScript and Data files

├── templates/ # directory with html files

├── __init__.py

├── app.py # incl. codes for upload files (C/MVC)

├── auth.py # incl. codes for register and login (C/MVC)

├── book.py # incl. codes for booking (MC/MVC)

├── staycation.py # incl. codes for packages (MC/MVC)

├── users.py # incl. codes for users (MC/MVC)

├── dashboard.py # incl. codes for display charts (MC/MVC)

├── forms.py # inlc. codes for handling forms using WTForm

├── requirements.txt # required libraries

└── venv/ # python environment

Consider the following codes that implements the Model using MongoEngine:

In __init__.py:

from flask import Flask

from flask_mongoengine import MongoEngine, Document from flask_login import LoginManager

import pymongo

def create_app():

app = Flask(__name__)

app.config[‘MONGODB_SETTINGS’] = {

‘db’:’eca’,

‘host’:’localhost’

}

app.static_folder = ‘assets’ db = MongoEngine(app)

app.config[‘SECRET_KEY’] = ‘9OLWxND4o83j4K4iuopO’ login_manager = LoginManager() login_manager.init_app(app) login_manager.login_view = ‘login’ return app, db, login_manager

app, db, login_manager = create_app()

In users.py,

from app import db

from flask_login import UserMixin

class User(UserMixin, db.Document):

meta = {‘collection’: ‘appUsers’} email = db.StringField(max_length=30) password = db.StringField() name = db.StringField()

In staycation.py,

from app import db

class STAYCATION(db.Document):

meta = {‘collection’: ‘staycation’} hotel_name = db.StringField(max_length=30) duration = db.IntField() unit_cost = db.FloatField()

image_url = db.StringField(max_length=30) description = db.StringField(max_length=500)

In book.py,

from users import User

from staycation import STAYCATION from app import db

class Booking(db.Document):

meta = {‘collection’: ‘booking’}

check_in_date = db.DateTimeField(required=True) customer = db.ReferenceField(User) package = db.ReferenceField(STAYCATION) total_cost = db.FloatField()

def calculate_total_cost(self):

self.total_cost = self.package.duration * self.package.unit_cost

(a) Produce comments to each of the above python programs that explains what and how the schema of the data model of the application is implemented. Cover all the following keywords or program statements in your comments:

• Those keywords bolded, such as “app.config[…]”, “db = MongoEngine(app)” and “meta”

• class User(db.Document), class STAYCATION(db.Document), class Booking(db.Document), and each of the attributes defined, including total_cost, etc.

• db.DataTimeField, db.InteField, db.FloatField, db.ReferenceField, and db.StringField • calculate_total_cost

(i) For the admin users, to upload the 3 data files and store the content in MongoDB.

(ii) For users, to book a staycation package and store the booking record in MongoDB.

(c) Re-develop your TMA solution to construct the application according to the design in Q1(b).

Question 2 concerns the re-factoring of the html codes that render the views according to the following directory structure under the templates sub-directory and the forms.py file:

/home/user/Projects/ECA └─ app

├── assets/

│ ├── css/ # directory with css files

│ ├── img/ # directory with image files

│ └── js/ # directory with JavaScript and Data files

├── templates/ # directory with html files

│ ├── __render_field.html # macro to render WTForms form

│ ├── base.html # the base html file

│ ├── login.html # that renders the login view

│ ├── register.html # that renders the register view

│ ├── packages.html # that renders the package view

│ ├── booking.html # that render the booking view

│ ├── upload.html # that renders the view for login

│ └── trend_chart.html # that renders the dashboard view

├── __init__.py ├── …

├── forms.py

├── …

└── venv/ # python environment

where forms.py contains the following codes:

from flask_wtf import FlaskForm

from wtforms import StringField, PasswordField, DateTimeField, FloatField from wtforms.validators import Email, Length, InputRequired

class RegForm(FlaskForm): email = StringField(‘Email’, validators=[InputRequired(), Email(message=’Invalid email’), Length(max=30)])

password = PasswordField(‘Password’, validators=[InputRequired(), Length(min=5, max=20)]) name = StringField(‘Name’)

and __render_field.html contains the following codes:

{% macro render_field(field) %}

&lt;div class=”form-group”&gt;

&lt;label for=”{{ field.name }} “&gt;&lt;h3&gt;{{ field.label.text.capitalize() }}&lt;/h3&gt;&lt;/label&gt;

{{ field(class_=’form-control’, **kwargs)|safe }}

&lt;ul&gt;

{% for error in field.errors %}

&lt;li style=”color:red;”&gt;{{ error }}&lt;/li&gt;

{% endfor %}

&lt;/ul&gt;

&lt;/div&gt; {% endmacro %}

(a) Provide comments on the above two files to explain how the codes work.

(b) Refactor and construct the code according to the provided structure below. The refactored html files contain all the source codes necessary for the rendering of all the views in the following 7 files:

• base.html

• login.htm

• register.html • packages.html

• booking.html

• upload.html • trend_chart.html

The admin user would like to have further insights into the popularity of the packages. Experiment with the visualization of data so the dashboard view would be added two more links to be clickable in the dashboard view sidebar component:

(a) Design and implement the View and Controller codes that produce the sidebar as required in Figs Q3(a), (b) and (c). The dropdown menu in Figure Q3(b) and (c) would contain all the user names registered and the hotel names of the packages in the website, respectively.

(b) Apply the data model as required in Q1(a) to implement the chart shown in Figure Q3 (b). The trend data is to be retrieved from the database.

(c) Apply the data model as required in Q1(a) to implement the chart shown in Figure Q3 (c). The trend data is to be retrieved from the database.

—– END OF ECA PAPER —–
