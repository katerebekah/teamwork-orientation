# User Stories

### What are User Stories?

Here's the format of a user story:

As a {user/group of users}, I need to {functionality}, in order to {larger goal}.

**Users**: Every piece of functionality for your app should relate back to a user or group of users. Users should drive the features you create, and you should never code anything that isn't directly related to a user requirement. This keeps you from writing unnecessary and unused code.

If you have a hard time determining who your users are, consider their role in your application: administrators, sellers, buyers, students, teachers, etc. 

> As a Bangazon administrator, I need to be able to view a list of all the sellers with their last log-in date in order identify inactive users.

Now, this user story will touch a couple areas of your code base, but it is one piece of functionality for your user. (See user stories vs. tickets below)

**Functionality**: This functionlity should be independent and provide value to the user. Setting up an api endpoint would not qualify as a User Story because you are not providing any independent functionality for your user. 

> As a vendor, I need be able to add an item to my inventory in order to make all my products available to customers

**Goals**: The goals here are the larger themes and requirements for the features you are implementing. These goals measure the *why* of your feature. If you are having a hard time determining why you are creating a feature, refer back to your requirements or think about what the feature gives to the user.

If you still have trouble thinking of a larger goal for your user story, reconsider the functionality part of the ticket and make sure it isn't too large. Sometimes it's easy to think of goal level objectives as functionality.

> As a buyer, I need to be able add items to lists in order to keep track of items I buy frequently or intend to buy in the future.

**Acceptance Criteria**: Acceptance criteria is a checklist of what needs to work in order for the ticket to be marked as complete. Sometimes the acceptance criteria is clear, but sometimes you can explicitly create a list of criteria within the user story. This clarifies what your user story is asking for and makes testing completion of your user story much easier.

### User Stories vs. Tickets

User stories are fully formed pieces of functionality and sometimes take many development tasks to be completed. Depending on the size of a user story, you can break the user story down into smaller tickets that address tasks necessary to complete a user story. For instance, you could have the following user story:

*(Create Account) As a user, I need to be able to create an account in order to have personalized content.*

This user story may be small enough to be completed by one developer in one sprint, but maybe it is too large. At this point you can break the user story down into a couple tasks that you'll use as tickets:

*Register Form (Create Account)*

*Angular controller form submit (Create Account)*

*Save User in Database (Create Account)*

Note that the tickets link back to the user story to give context to how the ticket fulfills a requirement. If you did a good job with acceptance criteria when creating your initial user story, you should be able to use one of the acceptance criteria per ticket.

### User story checklist

A good user story meets these criteria:

* Written from the perspective of a user 
* Answers the question of *why* 
* Simple and Consise
* Independent piece of functionality
* Clear acceptance criteria