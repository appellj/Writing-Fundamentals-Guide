# Lesson 1: Essentials of Technical Writing
In this lesson, we cover some of the essentials you should keep in mind when planning, writing, and releasing documentation and training content. 

## Plan a release based on feedback
At the beginning of a release, don’t just figure out what new features will be in the product and plan to doc those—also check with the rest of the product team to find out what areas they think need improvement from the last version of the documentation, and check user forums and support queries for the questions people are asking. Start working on improving this content right at the end of a release, before the next release is really underway when your time will be mostly focused on documenting new features.

## Work like an investigative journalist
When you’re first learning about a feature, work like an investigative journalist and focus on “getting the story.” Be curious and keep wondering what the user will ask next. Always ask and answer the question “why?”, and use the active voice wherever possible so that it’s absolutely clear who is doing what and when. For example, consider this sentence:

> The configuration must be updated to ensure all new users can access the application.

How does the configuration get updated? Does it happen automatically when a user signs up? Does an admin have to do it?

Instead, write this:

> When you add new users in the batch file, you must also update the configuration file to give these users immediate access to the application.

## Write for less-technical users
Developers often create products with a certain audience level in mind, and it can be easy to assume the audience is a lot more familiar with the company’s technology than they actually are. In reality, users often need more hand-holding and simple instructions than you might think. As you’re talking to an engineer or reading their spec or initial write-up, keep an image of a less-savvy user in mind and ask the questions that person would ask.

Never assume the user has read the introductory material, as they probably landed on that page by doing a web search. So make sure there are links back to the introductory material, definitions, etc. If someone unfamiliar with the product can understand it, you’ve communicated your message clearly.

## Put the most important information first
Start with the concepts they need to know (link off for more info), then how to do it, and then additional reference info. This follows the [inverted pyramid](https://en.wikipedia.org/wiki/Inverted_pyramid_(journalism)) with "Most Important/Newsworthy" at the top followed by "Important details" in the middle and "Other General Info/Background Info" at the bottom.

The first section of the topic should include this information:

* Basic overview of the feature
* What problem it solves/why this is useful (“so what?”)
* Example (if needed)
* Who should use this feature
* Very brief overview of “how”

Then go into the details after the intro. Let’s look at an example of a topic on remotely wiping a device:

> ### Remotely wiping a device
> The foo feature enables administrators to remotely delete all data and applications from a user’s device (also called “wiping” the device). This feature ensures that the data on your users’ devices will not be compromised if their device is lost or stolen. 

> A foo agent runs in the background on the user’s device and will therefore decrease battery life slightly, so it is most appropriate for users who a) have confidential data on their devices and b) do not need to maximize battery life. 

> After you enable foo on your server and install the agent on the user’s device, you can run foo from the Admin dashboard when you need to wipe the device.

> **To enable foo on the server:**
>
> 1. (instructions)
> 2. (instructions) 

> **To install the foo agent on a device:**
>
> 1. (instructions)
> 2. (instructions) 

> **To remotely wipe a device:**

> 1. (instructions)
> 2. (instructions)

You should name the topic based on what someone is trying to do. For example:

> Remotely wiping a device

is a more informative title than:

> Using the foo feature

## Refine the content
Warnings, gotchas, and prerequisites should appear before you tell them how to do something, never after. For example, imagine the support calls you’d get if you wrote this:

> To delete data:  
>
> 1. Navigate to **foo > bar**.
> 2. Enter your admin code.
> 3. Click **Delete**.
> 4. When prompted, click **Yes** to proceed.  
>
> Note: Only click Yes if you want to delete all the data in your system. You should make a backup before you do this.

Instead, you should write something like this:

> To delete all your data: 

> **WARNING!** These steps will permanently delete all the data in your system. 
>
> 1. Make a backup of your data. For details, see [Making a Backup](#).
> 2. Navigate to **foo > bar**.
> 3. Enter your admin code.
> 4. Click **Delete**.
> 5. If you are sure you want to delete all the data in your system, click **Yes** to proceed. 

> For information on restoring the data from your backup, see [Restoring Data](#).

Notice that the intro now indicates this will delete all your data, making a backup is part of the procedure so it’s harder to miss, and the confirmation step reiterates that this will delete all your data. Additionally, it includes a helpful link after the procedure that tells you how to restore your data in case you went through these steps and realized you didn’t actually want to do this. 

This approach puts the most important information first (there’s that inverted pyramid again), adds cues to help remind the reader what this is going to do, and anticipates a scenario where someone made a mistake. By thinking through what the reader wants to do and may inadvertently do, you can refine the content to be as helpful as possible. 

## Simplify the language
Cut out all extraneous words. For example:

* made arrangements for -> arranged 
* made the decision -> decided 
* made the measurement of -> measured
* performed the development of -> developed
* is working as expected -> works as expected

Break up long sentences and paragraphs. Use bulleted lists instead of listing options in a sentence, and use bold text to highlight the main points. Remember, readers aren’t here to read; they’re here to get the information as quickly as possible.

There’s a very nice example of this [here](https://cdn-images-1.medium.com/max/2000/1*72t2d-8wpxsT1zi7QlAEMg.png).

## Keep the reader’s goal in mind
Why are they here, and what do they want to know? For example, look at this sentence:

> This law was introduced in 2011, after a long, drawn-out process of appeals, to ensure that agency workers are given some of the same employment rights as their full-time counterparts.

In this example, the goal is for the reader to find out about employment rights. The information about the legal appeals process is not essential, so remove it:

> This law was introduced in 2011 to ensure that agency workers are given some of the same employment rights as their full-time counterparts.

Many developers want to provide as much specific detail as possible, but this can come at the expense of readers understanding the main point. For example:

> The system can process multiple requests per second. One customer processed 5,165,345 requests per second. Another customer processed 10,725,335 requests per second.

Instead, write:

> The system can handle enormous loads. One customer’s implementation regularly processes over 10 million requests per second, which was twice as much as their previous system could handle.

Remember, people want information, not just data. So give data as needed but always explain what it means. In this case, people want to know if it can handle very large loads, and giving the higher number as an example is sufficient, plus adding some info about why this number is significant (dig in and find out more about the example…in this case, it’s assuming you did your research and discovered that the load was twice the customer’s previous capacity).

Use the inverted pyramid for sentences as well. For example, instead of this:

> You can enter the information manually each time, but it’s better to configure it as a property.

Write this:

> Configure the information as a property so you don’t have to enter it manually each time.

## Use graphics wisely
Use screenshots when needed to orient the user, but don’t include them in every single step, or they can easily get lost. Animated GIFs are especially nice for showing how to navigate somewhere that’s hard to explain in text, but keep in mind that you must also add Alt text to all graphics to describe what’s happening in the image for those who are visually impaired.

## Examples are crucial
Have you ever noticed that you may read the first sentence describing a feature and still not really understand what it is, but then the next sentence gives a real-world example that helps you attach the concepts to something tangible? The best way to clarify your content is through examples. Not everything merits an example, while more complex concepts may need more than one example. When you’re documenting properties, giving examples of actual values helps a lot. And when describing how to write code, samples are essential.

## Test all the steps
It’s critical that you test and document all the steps in a procedure and not just rely on the steps that were given to you. People who know the technology well will often leave out small but important steps (such as restarting the server after making configuration changes), which results in support queries.

## Review your content
Walk away and then come back and reread your work to catch mistakes. And then always get a second pair of eyes on your writing. No matter how experienced you are, you will always make mistakes you can’t see, so peer reviews are important. They’re also a great way to catch gaps in your knowledge on grammar/punctuation rules. 

Likewise, whenever possible, get someone new to the technology to test out the procedures you’ve written.

Lastly, get a subject-matter expert to review your content to make sure you didn’t miss anything, and also ask for best practices that users should know. This approach will evolve your content from just covering the basics to being more deeply insightful and useful to advanced users.

## Get feedback from users
Look at the support queries and questions on user forums to see what people are asking and where they’re running into trouble.

## Summary
Our ultimate goal is to reduce support queries, so: 

* Ask good questions up front
* Structure the content using the inverted pyramid
* Write simple, accurate, fully tested content that gives information and not just data
* Provide good examples and graphics where needed
* Include best practices that will help users go beyond the basic steps

This approach will help ensure the users are successful and the support people are bored.

## Additional resources

* https://medium.com/@limedaring/five-tips-for-improving-your-technical-writing-and-documentation-47353723c8a7
* http://www.copyblogger.com/technical-writing/
* http://www.wikihow.com/Master-Technical-Writing
* http://web.mit.edu/me-ugoffice/communication/technical-writing.pdf
* http://idratherbewriting.com/2014/06/20/10-technical-writing-principles-to-live-by/
* https://tech.co/tips-technical-writing-2015-11

## 📘Assignment
1. In the documentation for your product, find a topic that could be improved.
1. Make changes using the principles above and send it to a writer for review. 
