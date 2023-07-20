# Tech Travelers Database Administration Application

Created using base code from the Nodejs starter app template from:
https://github.com/osu-cs340-ecampus/nodejs-starter-app

## Overview

TechTravels is a global online travel agency that connects customers with specialized travel agents to make their dream destinations a reality. Our remote agents are eager to advise and plan trips for their customers in several forms whether it be via phone, video call, email, messaging, or in-person meetings.

According to the US Travel Association, international travel spending reached $93 billion in February, following the pandemic.[1] By 2023, it is estimated that 700 million people will book their travel online, with 83% being Americans.[2] TechTravels has a team of 200 agents who book over 100,000 trip reservations annually and is expected to grow over time.

Our database-driven website will track our Customers and their Reservation details, such as Location, dates, and the travel Agents they are working with. That way, we will be able to monitor how many customers we have and their information, where our customers want to travel, and the number of reservations handled by each agent. Our database will also future-proof opportunities we may want to feature or enable such as studying trends of popular destinations or running reports to see which geographical area most of our customers come from.

[1] Mageau, Jamie. “The Latest Travel Data.” U.S. Travel Association, 30 Mar. 2023, https://www.ustravel.org/research/monthly-travel-data-report.
[2] “Top Guide to over 80 Online Travel Booking Statistics.” ConnollyCove, 22 Aug. 2022, https://www.connollycove.com/online-travel-booking-statistics/.

# CS340-TechTravelers
Project Title: TechTravels Destination Reservation Database Management

Team members:
<ul>
  <li>Sajidah Wahdy: Co-leader, database administrator, developer.</li>
  <li>Aylee Shomali: Co-leader, database administrator, developer.</li>
</ul>


## Executive Summary:
Our project design is a database solution for a remote travel agency to keep track of its customers, agents, reservations, and where its customers are traveling to. Throughout the term, we have made subtle changes to improve upon our work via various feedback. In six different steps, we started with our project idea and finished with a complete website for conducting CRUD operations using our designed database schema.

### Entity-Relationship Diagram:
<img width="856" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/41e9a70b-b3cb-4ac7-a9b9-37d27437a8c1">

### Schema:
<img width="886" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/1481bcc9-2dfe-46e3-9084-b1ae36d6709e">

### Sample Data:
<img width="894" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/ab0f1155-9af0-40b4-a287-5fc9ad3b018d">
<img width="869" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/10963a05-189c-4434-be9f-1d482a31dc3c">
<img width="895" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/06d41e07-ddef-4f2d-b287-4cceed649cbc">
<strong>Please note:</strong> We decided not to go into third normal form for our table structure and keep the transitive dependency between city names and country names in our locations table. This is because the probability of a country changing its name is very low, so we are not concerned about update anomalies here.

### UI Screenshots
#### Customers (FULL CRUD): Customers page
##### Read/Browse/Display
<img width="904" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/14e34046-0634-40a2-94d1-eb778d057373">

##### Create/Insert/Add New
<img width="908" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/b5a9fd32-1ebc-4af3-a1ee-2261640f7b07">

##### Update
<img width="859" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/3a774877-b473-4160-a03f-ae0f60fbd39a">

##### Delete
<img width="890" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/92b90e8a-be33-4c7e-b6e2-978e3c54aaf7">

#### Agents (FULL CRUD): Agents page
##### Read/Browse/Display
<img width="855" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/23cc35e7-8494-4ecb-8ff2-e8c97be168ae">

##### Create/Insert/Add New
Nullable relationship is the Location, Foreign Key attribute
<img width="851" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/1d951da7-7843-46a8-bf8f-72769b1dc09d">

##### Update
Includes Nullable relationship of Location
<img width="825" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/34c815b5-2b58-4b57-a40f-cb8523dceae2">

##### Delete
<img width="855" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/5a14b228-ea31-4f66-8dcf-02dcc5692e75">

#### Locations (CRD): Locations page
##### Read/Browse/Display
<img width="829" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/2ca8cd18-ce5f-44d5-84e5-5b4a9662fbce">

##### Create/Insert/Add New
<img width="834" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/e3ce526c-f643-474b-b0be-aa0992ac2ee0">

##### Delete
<img width="822" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/4174fd62-da32-4137-bd08-8dca020c99c5">

#### Reservations (CRD): Reservations page
##### Read/Browse/Display
<img width="826" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/7ea56b59-36b9-441b-8422-2283328c5728">

##### Create/Insert/Add New
Dynamic dropdown functionality for Agent Foreign Key includes Nullable relationship of Agent
<img width="829" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/d7e47914-d48e-472c-a754-d9406c645a66">

##### Delete
<img width="824" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/5e57ac53-906d-40a6-99e1-dc8812d8c71d">

#### CustomerReservation (CRD): CustomerReservation page
M:N relationship between Customers and Reservations

##### Read/Browse/Display
<img width="825" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/d367a0c8-d325-4bc0-8d0a-e4fb38096f1c">

##### Create/Insert/Add New
Dynamic dropdown functionality for Customer and Reservation FKs
<img width="849" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/b773c6b6-893c-463f-84aa-da1c62be3756">

##### Update
Dynamic dropdown functionality for FKs, Update for M:N relationship
<img width="863" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/11670043-a63f-4c90-9dd2-b3f88c1ec615">

##### Delete
Deleting from an M:N relationship
<img width="830" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/afc28194-6a7b-4fb9-96c0-f8eeda4f33cd">

#### ReservationLocation (CRD): ReservationLocation page
M:N relationship between Reservations and Locations

##### Read/Browse/Display
<img width="826" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/30e08d01-271e-45e0-b6d6-0a320fbe287f">

##### Create/Insert/Add New
Dynamic dropdown functionality for Location and Reservation FKs
<img width="827" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/57cf89cb-933e-4d2a-9c6f-ad03be5696c6">

##### Delete
Deleting from an M:N relationship
<img width="828" alt="image" src="https://github.com/sajidahw/TechTravelers/assets/88634981/1dbb1a99-9e6f-43a8-b362-593dd69d4b19">
