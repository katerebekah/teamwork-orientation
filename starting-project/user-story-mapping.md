# User Story Mapping

User Story Mapping is a tool to visualize the stories you tell about your software. It's a valuable tool in planning a project from scratch. We're going to walk through the process and give examples using a prospective project called the Bangazon Admin Tool.

## 1. **Synopsis** 
Outline your project idea. Brainstorm on the *why* of your project: Why make this product? What is the problem you are trying to solve? What are the benefits to your users? Write down the high level parts of what your project is doing to do and why you're making it.

> **Bangazon Admin Tool**: The app is a feedback tool between students and teachers designed for the Bangazon curriculum. It's purpose is to give students and instructors a place to give and receive feedback with a full history of their interactions, because collaboration between students and instruction staff is essential for successful student outcomes. 

## 2.  **Personas**
Consider your project's potential user groups. Make a sample persona for each group of user and list the activities, pain points of their current system, and any additional notes about the persona. It's common to use large sticky notes, cards, or a whiteboard for this process.

> **Sally Student**, an active student user
> **Activities**: Give feedback, Receive feedback, Self-assess progress
> **Pain Points**:  Slack's messaging archive prevents storage of conversation history. Feedback on GitHub pull requests doesn't give full story of entire student progress. There's no easy way to give instructor feedback except for in milestone surveys.
> **Notes**: Slack integration would be helpful for this user. Not likely to want to log into another app.

> **Molly Manager**, an instructor manager of Bangazon team
> **Activities**: Give student feedback, track student progress, receive student feedback, track team progress, compare student self-assessments for trends
> **Pain Points**:  Slack's messaging archive prevents storage of conversation history, hard to consistently track student progress beyond pull requests, uncertainty about whether there's adequate instruction coverage of a topic.
> **Notes**: Again, slack integration would be helpful with a bunch of the functionality. Github integration for code review.

> **Andy Administrator**, the school administrator
> **Activities**: Tracking student progress, track team and cohort progress, measuring outcomes across cohorts
> **Pain Points**:  Not being in the classroom prevents knowledge about student progress until there's a notable problem. It's hard to track school progress without a birds-eye view of student info.
> **Notes**: This person will need a more in-depth UI for accessing Givecomplex student data. A dashboard with pressing items to review and data visualizations will present data efficiently and not waste valuable time.

## 3. **Map the Stories**

You should have 4 colors of sticky notes. Here's how they are color coded: Personas as one color, activities as another, major tasks (called the backbone) as third, and technical tasks as fourth.

You'll be making a tree-like structure with your sticky notes. Start with your first persona. This is a sample map for one persona for the Bangazon Admin Tool:

    [ Sally Student ]

        [ Give Feedback ]
            
            [ Ability to submit a basic feedback form ]
                [ HTML Feedback form - MVP ]
                [ One text box for feedback - MVP ]
                [ Submit button - MVP ]
                [ Api endpoint to save feedback - MVP ]
                [ Store in DB - MVP ]
            
            [ Ability to give 1 - 5 star rating ] 
                [ Update form to add basic star rating using dropdown list - MVP ]
                [ Update form saving in DB to add star rating - MVP ]
                [ Update star rating HTML component to look nice ]
            
            [ Ability to link feedback to instructor ]
                [ Retrieve list of instructors for student ]
                [ Update form to have dropdown list of instructors ]
                [ Update form saving in DB to add instructor ]
            
            [ Ability to link feedback to a milestone ]
                [ Retrieve list of milestones for student ]
                [ Update for to have dropdown list of milestones ]
                [ Update form saving in DB to add milestone ]
            
            [ Ability to add additional content (update) to old feedback ]
                [ Ability to see list of old feedback ]
                [ Ability to add addendum text to feeback ]
                [ Ability to update star rating on feedback ]

            [ Ability to add feedback through Slack ]
                [ Slackbot commands for adding feedback ]
                [ Slackbot commands for updating feedback ]

        [ Receieve Feedback ]

            [ Ability to see list of instructor feedback ]
                [ Retrieve feedback for student - MVP ]
                [ Show list of feedback - MVP ]
                [ Ability to see feedback details - MVP ]

            [ Receive notifications about new feedback ]
                [ Show feedback in order of newest to oldest in list - MVP ]
                [ Slack notification ]
                [ Slackbot command for seeing feedback ]

            [ Ability to respond to feedback ]
                [ Form to respond to feedback - MVP ]
                [ Message threading ]
                [ Slackbot ability to respond to feedback ]
                [ Slackbot ability to see feedback response thread history ]

        [ Self-Assess Progress ]

            [ Ability to rank your comprehension on a milestone ]
                [ Ability to see list of milestones - MVP ]
                [ Ability to use a dropdown list to give your comprehension rating (1 - 5) - MVP ]
                [ Update comprehension rating to use star rating component ]

            [ Ability to rank your comprehension on a milestone subtopic ]
                [ Ability to see list of subtopics for each milestone - MVP ]
                [ Ability to use a dropdown list to give your comprehension rating (1 - 5) - MVP ]
                [ Update comprehension rating to use star rating component ]

            [ Ability to update your comprehension rating ]
                [ Form to update your comprehension rating - MVP ]
                [ Slackbot command to update comprehension rating ]

            [ Ability to leave comments about comprehension rating ]
                [ Have comments text box for each comprehension rating - MVP ]
                [ Add star rating and comments section to modal to better organize page ]

            [ Ability to link github repos to comprehension rating ]
                [ Ability to add links to github repos with textboxes in modal ]

**Note:** in the brainstorming process, several items were added to the map that will take many sprints to complete. It's important to see which tasks are necessary for MVP and which are stretch goals.

> Stretch goals add significant value to an app, but aren't necessary for the app to do its job.

I've labelled which tasks are MVP. You'll notice what isn't MVP falls into a few major areas: targeted feedback options, slack integration, and UI visual enhancements. After MVP is completed in the development process, the next highest priority would be completed next.


## 4. **Record your results**

You'll notice that each of the technical tasks is a very granular bit of functionality - independent and small. Take these to make your user story tickets in your GitHub projects, Trello, or other ticketing system. 

## 5. **Begin Development**

This process has given you a backlog to start building your projects. At this point it's time to follow your sprint procedures to begin your development on your project.