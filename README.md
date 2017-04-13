# assignment_designing_nosql_data_models
I'll have one data model hold the SQL please


Egle Libby
Renzo Tomlinson

Basic
* User
    * _id
        * <ObjectId>
    * username
        * <string> Must contain 6-12 word characters
    * password
        * <string> Must contain 7-12 word character and at least one uppercase
    * email
        * <string> Must contain @ character
    * profile
        * birthday
            * <Date>
        * gender
            * <string> M or F
        * phone number
            * <number> 10 digits Only US numbers
        * location
            * city
                * <string>
            * state
                * <string> Two letters state code
            * country
                * <string> Only word characters
        * about
            * <string> Max 140 characters
    * visibility-settings
        * birthday
            * boolean
        * gender
            * boolean
        * phone number
            * boolean
        * location
            * boolean
* LoggedInUsers
    * IsLoggedIn
        * <Array> of ObjectIds of users that are logged in


<!--You're building an application that requires user login. Once logged in the user has a bunch of profile information and preference settings available to them. They will need to be able set their birthday, gender, phone number and location (city, state, country). They should be able to provide text to tell about themselves. They also should be able to enable and disable visibility of their birthday, gender, phone number and location.-->

<!--Intermediate-->

<!--You're building a restaurant table reserving app that allows users to reserve tables for specified numbers of people. The app will need to show only tables that are available and the times they are available. The app will need to store reservations under a given name with a phone number and number of guests.-->

Need to know
What table are available and at what times? Max number of guests per table
If a table is reserved, we need to know who reserved the table and what his/her phone number is and number of guests

* Tables
  * <array> of table objects
    * Table
      * id
      * max-capacity
        * <number>
      * available times
        * <array>
      * reserved times
        <array>

* Reservations
  * <array> of reservation objects
    * Reservation
      * id
      * table id
      * time
        * <date>
      * number of guests
        * <number> has to be less than or equal to max-capacity of table associated with table id
      * reserver
        * name
          * <string>
        * phone number
          * <number>

<!-- You're building a backend for a university that requires students to be able to login. Once logged in, the students can view the exam grades for their classes. They should be able to view results by semester. Each semester should only show the classes in which that student is enrolled that semester.
 -->

* Students
  * <array> of student objects
    * Student
      * id
      * username
        * <string>
      * password
        * <string> 7-12 word characters
      * <array> of Semester object
        * Semester
          * id
          * <array> of class object
            * Class
              * id
              * grade


<!-- Advanced -->

<!-- Your eCommerce business needs to keep track of products and their prices. The products each belong to a department. The business needs to keep track of revenue as product prices change over time. The business also needs to keep track of receipts of transactions and the number of units each product has in stock. -->

* Products
  * <array> of product objects
    * Product
      * id
      * name
      * current price
      * <array> of historic price objects
        * Historic price
          * date
            *<date>
          * price
            * <number>

* Departments
  * <array> of department objects
    * Department
      * id
      * <array> of product id

* Business
  * <array> of transaction objects
    * Transaction
      * id
      * date
      * product id
      * number of units sold
      * product price
  * <array> of inventory objects
    * Inventory
      * product id
      * stock

<!--You're building an activity feed for a social media site. The feed must display a chronological list of activities for the current user's friends. These activities could potentially be any action performed on the site including uploading a photo, changing their profile, friending another user, commenting, liking etc... Further, you only want to display activities for users that the current user interacts with frequently.-->

What do we need
User has feeds, we need to know friends activities, and frequency of interaction
Per friend's activity we need to know what time it occurred and friend frequency score


* User
    * id
    * Feed
        * <array> of friends activities
            * friends_id
                * <number>
            * time
                * <Date>
            * type of activity
                * <string>
    * Friends
        * <array> of friend + frequency score
            * friends_id
                * <number>
            * frequency_score
                * <number>
    * Activities
        * <array> of activities
            * id
                * <number>
            * type of activity
                * <string>






