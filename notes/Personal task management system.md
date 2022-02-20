
# Personal task management system

## Why?

For me, the most important reason to maintain a list of tasks is to get things out of my head so that I don't forget them and stop stressing about them.

1. **Quick entry** - There should be a place to dump things that come to mind but can't be worked on right away, even trivial things like replying to important messages/emails. Once this becomes habitual, it allows the mind to relax and enjoy the moment.
2. **Task filters** Once the dump habit takes hold, there should be a way to select 2-3 things to work on today.

For (1), voice entry or some kind of a quick task entry dialog is useful, without forcing a triage (of priority, due date).
For (2), I need three minimum features.

2a. **Task priority**

2b. **Start date / scheduled date / threshold date** : Hide tasks until some future date. This feature is insanely useful but surprisingly uncommon in most task managers. I cannot imagine using a task manager that doesn't support this. Toodledo, Remember the Milk, https://swiftodoapp.com/todotxt-syntax/due-dates-and-threshold-dates/, https://www.omnigroup.com/omnifocus/ are the ones I know that support this feature.

2c. **Mobile notifications / reminders** - For some tasks, it really comes down to a specific time, like birthdays, school pickups etc. Technically, these could go to a calendar entry but having reminders via notificaitons on mobile devices within task managers keeps it all in one place.

Apart from these, support for recurrences are useful if you want to also track routine stuff like credit card bills, garbage day etc.

## How? Remember the Milk
Remember the Milk's free plan checks all these boxes for me (see more on reminders below). It looks clean but supports quite a bit of complexity. It's been around long enough that they've hopefully settled on a sustainable business model. They have clients for all platforms including web.

#### Quick entry
RTM has a fairly easy way to enter tasks both in the web UI and mobile clients. Voice entry is possible with Siri (iOS) and is a good reason to upgrade to their paid plan.

#### Current tasks view
Remember the milk has an Inbox view but I set my start page to a saved search (what they call a "smart list") that looks something like

```(priority:1 OR priority:None) AND (startBefore:Today OR start:empty) AND (list: Inbox OR list: regularhome)```

This is a prioritized list that avoids future tasks and includes quick-entry tasks with no priority. This forces an automatic triage of quick-entry tasks and they drop off this list once prioritized or postponed by start date.

#### Task reminders
Remember the milk supports mobile notifications for task reminders in their paid plan on mobile devices. Reminders are triggered when a task has a due **time** in the **due date** field - the web UI doesn't make this clear.

You can also accomplish something close to reminders in their free plan by enabling email/text reminders. SMS reminders never worked for me but email reminders do. I want mobile notifications for just Remember The Milk, so I use the [VIP alerts](https://support.apple.com/en-al/HT207213#vip) feature in iOS to enable mobile notifications specifically for remind@rememberthemilk.com  

#### Other useful RTM features

RTM has one of the best balance between free and paid plans. They make their free plan quite useful - sharing a task list with your spouse is possible, for example. At the same time, mobile notifications, viewing completed tasks for more than 7 days and Siri integration are all valuable features that can compel users to sign up for a paid plan.

## Alternatives

1. **[Toodledo](https://www.toodledo.com)** was my previous favorite and I used to pay for it. The UI design is more plain but it supports all the key features. The only slight negatives are that saved search is a paid feature and their mobile sync has a few rare issues. They also had some kind of a management change recently, hopefully it will stabilize at some point.
2. **[Obsidian tasks](https://schemar.github.io/obsidian-tasks/)** Task managers should technically be implementable with a csv file or spreadsheet and some custom filtering logic on top of it. Obsidian tasks comes close to this idea but there's two problems with this approach - mobile notifications aren't supported (yet) and the task format could use improvement (the use of unicode chars, priority has to be the last character). The nice part is that saved searches are supported through a very [flexible interface](https://schemar.github.io/obsidian-tasks/queries/filters/. I hope this can be made workable at some point in the future because that would allow tasks and related notes to be kept in the same place and it would make it one less service to sign up for.
3. **Pen and paper** is a school of thought that is a popular alternative that gets mentioned on Hacker news frequently. I've tried it but found it consistently inferior because of the lack of text search and accessibility. 
4. [todo.txt](http://todotxt.org/) is similar to the obsidian tasks approach of plain-text files with app processing logic on top. But it doesn't support a start date in the standard. [SwiftDo](https://swiftodoapp.com/) technically extends it to support a start date but I haven't tried it yet.



