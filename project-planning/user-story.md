# User Stories

### What are User Stories?

Here's the format of a user story that you will be provided with by your stakeholder.

As a {user/group of users}, I need to {functionality}, in order to {larger goal}.

**Users**: Every piece of functionality for your app should relate back to a user or group of users. Users should drive the features you create, and you should never code anything that isn't directly related to a user requirement. This keeps you from writing unnecessary and unused code.

If you have a hard time determining who your users are, consider their role in your application: administrators, sellers, buyers, students, teachers, etc. 

> As a Bangazon administrator, I need to be able to view a list of all the sellers with their last log-in date in order identify inactive users.

Now, this user story will touch a couple areas of your code base, but it is one piece of functionality for your user.

**Functionality**: This functionlity should be independent and provide value to the user. Setting up an api endpoint would not qualify as a User Story because you are not providing any independent functionality for your user. If your tickets seem too large, try using the [Relative Sizing Process](./relative-sizing.md) to determine if you should split any user stories into multiple tickets.

> As a vendor, I need be able to add an item to my inventory in order to make all my products available to customers

**Goals**: The goals here are the larger themes and requirements for the features you are implementing. These goals measure the *why* of your feature. If you are having a hard time determining why you are creating a feature, refer back to your requirements or think about what the feature gives to the user.

If you still have trouble thinking of a larger goal for your user story, reconsider the functionality part of the ticket and make sure it isn't too large. Sometimes it's easy to think of goal level objectives as functionality.

> As a buyer, I need to be able add items to lists in order to keep track of items I buy frequently or intend to buy in the future.

### User story checklist

A good user story meets these criteria:

* Written from the perspective of a user 
* Answers the question of *why* 
* Simple and Consise
* Independent piece of functionality

## Acceptance Criteria

Acceptance criteria break down the user story into the individual behaviors and affordances of the feature you are building. They will be written using the [Behavior Driven Development](https://en.wikipedia.org/wiki/Behavior-driven_development) language of **Given** - **When** - **Then**.

Here's an example of a user story and it accompanying accetance criteria.

#### User Story

**As** an application administrator

**In order** to manage the permissions of individual users

**I want to** have a view that lists all users, their current permission level, and an affordance to change the permission level

#### Acceptance Criteria

**Given** that a user is authenticated

**And** the user is authorized as an administrator

**When** the user visits any page in the application

**Then** there should be a hyperlink in the top navigation bar titled *User Permissions*

---

**Given** that a user is an authenticated adminsitrator

**When** the user clicks on the *User Permissions* navigation bar hyperlink

**Then** the user should be presented with a list of all current users

**And** each user should be labeled with their current permission level

**And** there should be a dropdown element next to each user that contains an option for each available permission level

---

**Given** that an authenticated adminsitrator is viewing the *User Permission* page

**When** the user selects a permission level from the permission dropdown list next to a user

**Then** the user should be updated with the new permission level

**And** the view should be updated automatically to reflect the new permission level