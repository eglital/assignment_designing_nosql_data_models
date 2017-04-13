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


*



