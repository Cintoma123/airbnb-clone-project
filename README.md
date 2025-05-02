# airbnb-clone-project
An airbnb clone built for learning software enginnering
# Team Roles
Software developer :
Engineers and stabilizes the product
Solves any technical problems emerging during the development lifecycle

DevOps engineer :
Facilitates cooperation between development and operations teams
Builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery

UI/UX designer:
Transforms a product vision into user-friendly designs
Creates user journeys for the best user experience and highest conversion rates

Database Administrator (DBA) 
is responsible for the overall management, maintenance, and security of databases within an organization.
They ensure that data is stored correctly, accessed securely, and performs efficiently,
while also collaborating with developers and business users. Key responsibilities include backup and restoration,
database design, security management, and troubleshooting. 

Front-end software engineer:
Ensure the technical feasibility of UI/UX designs. Optimize applications for maximum speed and scalability.
Collaborate with team members and stakeholders to balance aesthetic choices with technical challenges. 
Maintain and improve the website, prioritizing user experience

# Technology Stack
Django : is software you can use to develop web applications quickly and efficiently.
Most web applications have several common functions, like authentication, 
information retrieval from a database, and cookie management. 
Developers have to code similar functionality into every web app they write.

PostgreSQL : allows functions that have named parameters to be called using either positional or named notation.
Named notation is especially useful for functions that have a large number of parameters,
since it makes the associations between parameters and actual arguments more explicit and reliable.

GraphQL : is a query language and server-side runtime for application programming interfaces (APIs) 
that gives API clients exactly the data they requested.
As an alternative to REST, GraphQL allows developers to 
make requests to fetch data from multiple data sources with a single API call.

REST APIs : communicate through HTTP requests to perform standard database functions 
like creating, reading, updating and deleting records (also known as CRUD) within a resource. 
For example, a REST API would use a GET request to retrieve a record. 
A POST request creates a new record.

MySQL : is an open source relational database management system (RDBMS) that's used to store and manage data. 
Its reliability, performance, scalability, and ease of use make MySQL a popular choice for developers.

# Database Design
The key entities required for the project includes:
Users
Properties 
Bookings 
Reviews
and Payments.

 Database Design

Users:
Fields:
   id (Primary Key)
   name
   email
   password
   created_at
  Relationships:
   A user can own multiple properties.
   A user can make multiple bookings.
   A user can leave reviews on properties.

 Properties:
 Fields:
   id (Primary Key)
   title
   location
   price_per_night
   owner_id (Foreign Key referencing Users)
Relationships:
   A property is owned by one user.
   A property can have multiple bookings.
   A property can receive multiple reviews.
   
 Bookings
Fields:
   id (Primary Key)
   user_id (Foreign Key referencing Users)
   property_id (Foreign Key referencing Properties)
   start_date
   end_date
Relationships:
A booking is made by one user for one property.

 Reviews
Fields:
   id (Primary Key)
   user_id (Foreign Key referencing Users)
   property_id (Foreign Key referencing Properties)
   rating
   comment
   Relationships:
   
Payments
Fields:
   id (Primary Key)
   user_id (Foreign Key)
   booking_id (Foreign Key)
   amount
   status
  Relationships:
 A payment is made by a user for a booking.

 # Feature Breakdown

1. User Management
This feature handles user registration, login, and profile updates. It ensures secure access to the platform and stores personal user information for booking and reviewing properties.

2. Property Management
Allows hosts to list their properties, upload descriptions and images, and set availability and pricing. This is a core feature that drives the rental offerings of the application.

3. Booking System
Enables users to book available properties for selected dates. It manages conflicts in booking times and ensures payment is tied to a valid reservation.

4. Review System
Users can leave reviews and rate properties they’ve stayed in. This promotes transparency and helps other users make informed decisions based on past guest experiences.

5. Payment Integration
Handles secure payment processing for bookings. It ensures that users are charged correctly and that hosts receive payments based on booking agreements.
