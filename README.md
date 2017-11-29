# assignment_data_modeling

Mmmmm.... dataaaaa.... Jeffrey Dederick _Include your ERM modeling "pseudocode"
in the space below_

=== Basic ===

1. Goals: Users need to be able to access all courses Each course needs to be
   able to access all lessons.

Entities:

* courses
* lessons

Attributes:

* course id (integer - primary key)
* course title (string 12-36) course
* description (string 100max)

* lesson id (integer - primary key)
* lesson title (string 12-36)
* lesson body (string 10,000max)
* course id (integer - foreign key)

Relationships:

* One (courses to many (lessons)

2. Users should have 1 profile.

Entities:

* Users
* Demographics

Attributes:

* user id (integer - primary key)
* username (string 8-24)
* email (string 12-36)

* demographics id (integer - primary key)
* city (string 12-36)
* state (dropdown)
* country (string 5-36)
* age (integer 2-3)
* gender (set options - male or female)
* user id (integer - foreign key)

Relationship:

* One (user) to one (demographics)

=== Intermediate ===

1. Entities:

* Users
* Posts
* Comments

Attributes:

* user id (integer - primary key)
* username (string 8-24)
* email (string 12-36)

* post id (integer - primary key)
* post title (string 12-36)
* post body (string 10,000max)
* user id (integer foreign key)

* comment id (integer - primary key)
* comment body (string 500max)
* post id (integer foreign key)
* user id (integer foreign key)

Relationships:

* One (users) to many (posts)
* One (posts) to many (comments)
* One (users) to many (comments)
* One (comments) to many (comments)

Advanced

1. Entities:

* Products
* Users
* Orders
* Shipments

Attributes:

* user id (integer - primary key)
* username (string 8-24)
* email (string 12-36)

* shipping address id (integer - primary key)
* address (string 12-36)
* city (string 12-36)
* state (dropdown)
* country (string 5-36)
* user id (integer - foreign key)

* payment id (integer - primary key)
* payment type (dropdown)
* card number (integer 12-36)
* card type (dropdown)
* billing address (string 12-36)
* billing city (String 12-36)
* billing state (dropdown)
* billing country (string 5-36)
* user id (foreign key)

* order id (integer - primary key)
* shipping address id (integer - foreign key)
* user id (integer - foreign key)
* shipment id (integer - foreign key)

* join table (payments, orders)
* order id (integer)
* payment id (integer)

* join table (orders, products)
* product id (integer)
* order id (integer)

Relationships:

* One (users) to many (orders)
* One (users) to many (shipping address)
* One (users) to many (payments)
* One (shipping address) to many (orders)
* Many (payments) to many (orders) - join table
* Many (orders) to many (products) - join table
* One (shipment) to many (orders)

What happens to historical data if user deletes their account? Primary keys for
obsolete data will never be reused. ???
