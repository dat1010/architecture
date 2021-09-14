## The Multisect

<img src="https://static.wikia.nocookie.net/marveldatabase/images/1/18/Multisect_from_Marvel_2-In-One_Vol_1_2_001.jpg/revision/latest?cb=20180127000625" width="10%" length="10%">
The Multisect is a fictional tool in the Marvel Universe. It can access an area called Multiplane. The door to infinite universes.

Multisect the Elixir program can create many tables and CRUD endpoints to access those tables.
This will provide a simple user interface to create a table with string or integer options. Once that table is created a route is available
for the creator of the table to easily access.

### Architecture Designs

1. Elixir API service
2. Guardian Authentication
3. Uses [Hasura](https://github.com/hasura/graphql-engine)


### Architecture Structure

1. Setup [Altlantis](https://www.runatlantis.io/) in private github repo
2. Setup [Terraform](https://www.terraform.io/) for iam infrustructure 
3. Setp [Terraform](https://www.terraform.io/) for multiplane infrustructure


### Architecture

#### Diagram

<img src="https://github.com/dat1010/architecture/blob/main/Multisect/Multistet.png" width="75%" length="75%">


#### Multiset Service API
This will be an Elixir API that allows an authorized user to create
[API](Multisect/API/README.md)

#### Migration Service
This service will pull consume from the sqs.
Once that message has arrive it will look in the apropriate table and generate a migration in the database for that user.

