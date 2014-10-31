# Event Management Application

This project has been designed to take roughly 8 hours. Feel free to take more time if you need it. Please **DO NOT** fork this project, instead clone a fresh copy and submit a zip file with your work.

## Requirements

You are responsible for building the back-end CRUD interace only; thus you do not need to implement any `show` actions.

* The application must be built with **Ruby on Rails**.
* You may use **Twitter Bootstrap** or **Zurb Foundation** (Bootstrap 3 is included by default in this project).
* User authentication is not required for this application.

## What we're looking for...

* Understanding of basic user flows and application design (MVC)
* Knowledge of the Ruby programming language, data modelling techniques, and the Rails framework
* Sense of web development best practices

## Mockups

There are a set of [basic mockups](https://github.com/RobotsandRockets/event-manager/raw/master/doc/mockups.pdf) available which should serve as a visual guideline for what you're building.

## Data Models

![Entity Relationship Diagram](https://raw.githubusercontent.com/RobotsandRockets/event-manager/master/doc/erd.png)

## API Endpoint

You *must build an API endpoint* for allowing a visitor to RSVP for an event. This endpoint should take the **name** of the attendee and an optional **number of guests**.

## Image Uploads

For this project, the user should be able to upload images. You may want to look into [CarrierWave](https://github.com/carrierwaveuploader/carrierwave) or [Paperclip](https://github.com/thoughtbot/paperclip) to accomplish this.

It is sufficient to upload files directly to the filesystem for storage (instead of a CDN). Thumbnail generation is optional, but appreciated.

## Pages

### Events Index/Listing Page

This page should show all events in the system *except cancelled events* and should be divided into two tabs: **upcoming** events and **past** events.

The list should be **paginated** and allow the user to click into the _event detail page_.

### Event Detail Page

This page should allow the user to create a new event or edit an existing one and is divided into three tabs: **event details**, **photos**, and **attendees**.

#### Event Details Tab

This should allow the user to add the following data about an event:

* Event Title
* Image
* Speaker
* Description
* Location (street 1, street 2, city, state, zip)
* Start date & time

If the event has already been created, the user should have the ability to **cancel** the event, which flags it as cancelled and hides it from the _list view_.

If the event is new, the app should validate the presence of the event's title, description, location, and start date/time (must be in the future).

#### Event Photos Tab

This tab is unavailable until the event has been created. This screen should allow the user to upload any number of photos and **optionally add a caption** to them. The user can also delete the photos.

See the section on [image](#image-uploads) for specifications.

#### Event Attendees Tab

This tab is unavailable until the event has been created. This screen should list event attendees that have been submitted via the [API endpoint](#api-endpoint) described above. It should also allow the user to **remove attendees**.
