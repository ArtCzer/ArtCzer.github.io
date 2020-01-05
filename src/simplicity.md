# 04/01/2020
## Refreshing
Last week I spend the Christmas holidays with my family, fishing and surfing in the Northern Rivers region on the east coast of Australia. 

In our work, and to a lesser extent outside of work, it's increasingly normal to be beholden to a rigid timetable of goals, meetings, tasks and trello boards. 

Spending a week without any due dates or timetable was refreshing, and made me appreciate the simplicity of unplanned time. 
I kept busy - going to the beach at least once day day, fishing, shopping and cooking, but without the pressure of a strict timeline. 

In software engineering, this kind of unplanned (but productive) time can be just as refreshing, and can be uniquely productive. 

That's why great software companies allow their engineers time to work on their own tasks, without the pressure of deadlines or external business requirements. Examples of this are hackathons, passion projects, coding competitions and personal development time.

...

# 5/01/2020
## Simplicity - Static Website and templating engine
As engineers, each year we learn to use dozens of new tools, while simultaneously a lot of the stuff we learnt only 1-2 years ago become obsolete and forgotten. 

A key principle that I use to guide me in making technical decisions is to keep in mind the 'KISS Principle', or more accurately, as Einstein quoted: 'Everything should be made as simple as possible, but no simpler.'

Often we don't take into account the tradeoffs between creating a simple soution versus building or learning a framework. 
Using a framework has several risks
1. Takes time to learn, which could be better spent releasing the MVP
2. Technical risk of maintaining and upgrading the framework 
3. Copgnitive complexity, and the resources required to maintain it
4. Future requirements unable to be met by the framework - necessitating a migration to a new framework

If your needs are simple, then your solution should match that simplicity.

If all you need is a static site, and it will remain reasonably static for the foreseeable future, there's nothing wrong with just hand written HTML/CSS hosted on a storage provider / CDN. This has the benefit of
* Fast development time
* Cheap and simple depolyment
* Easy to maintain or migrate in future
* Security

 When maintenance becomes a chore, you'll want to build the robot to make your life easier.

 Rather than learn a complex tool like Jekyll https://jekyllrb.com/docs/, I'm going to create my own minimal site builder custom made for my needs, in less time than it would take to install, build and configure a third party framework.

 Steps
 1. npm install the packages
 2. write a script to process markdown files and convert to HTML
 3. webpack

