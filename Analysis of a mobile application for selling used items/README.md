## Project description
I am a junior analyst at "Unnecessary Things" company. Our company has developed the "Unnecessary Items" application to make it possible to post ads and sell used items for sellers and purchase used items for buyers.

**Research customers** are project managers who are involved in increasing user involvement in this application.

**The goal of project managers** is to segment users into audiences in order to more effectively influence individual user segments in the future.

## Research objectives.

**1. Analyze the connection between the target event - viewing contacts - and other user actions, namely:**
- In the context of sessions, select scenarios\patterns that lead to viewing contacts.
- Build funnels based on main scenarios in the context of unique users
- How does the time differ between the events "map -> contacts_show and search -> contacts_show" within sessions?

**2. Assess what actions are most often performed by those users who view contacts, namely:**
- Calculate the relative frequency of events by user groups with and without event "contacts_show".

## General conclusion.
As a result of the study, the behavior of application users was analyzed based on user logs, as well as the results of A/B tests.

After data preprocessing, the behavior of 1843 users of the mobile application was examined over a period of 28 calendar days (from 2019-10-07 00:00:00 to 2019-11-03 23:58:13).
User sessions were allocated / session length was determined to be 30 minutes according to information in Google Analytics.
The target action of this analysis is the action in the `show_contacts` application

It was revealed that:
- the number of unique users is actively growing from weeks 41 to 43, which is a good sign, but starting from week 44, the number of users began to decline, which may be an alarming sign
- The average session duration is 2 minutes and 10 seconds (130 seconds).
- Average number of events per user = 10.0
- Conversion of visitors who completed the target action = 22.85%


A Sankei diagram was also constructed to identify the main scenarios that lead to the target action.

Main scenarios that lead to the target action.
- Script `photos_show` -> `show_contacts` / conversion to target action for this script was 16.52%
- Script `tips_show` -> `show_contacts` / conversion to target action for this script was 11.4%
- Script `map` -> `tips_show` -> `show_contacts` / conversion to target action for this scenario was 6.84%
- Script `search` -> `tips_show` -> `show_contacts` / conversion to target action for this scenario was 4.35%

The most effective scenario leading to the target action is photos_show -> show_contacts with a conversion of 16.52%

Additionally, the relative frequency of events was calculated by user groups with and without contacts_show:
- The most common action for the two user groups (those who do and do not perform the `show_contacts` action) is the `tips_show` action, but the relative frequency of this event for the two user groups is different:
         - group C `show_contacts` - performs this action in about a third of all actions (35% of all actions).
         - group WITHOUT `show_contacts` - performs this action in more than half of all actions (56% of all actions).

- the user group C `show_contacts` has the action `contact_call`, which indicates that often after viewing contracts, a call is made regarding the advertisement. It might be worth reconsidering the target action from `show_contacts` to `contact_call`.

- the lowest relative action for the two groups is `tips_click` (clicked on a recommended ad). Recommended ads are seen, but for some reason they are not clicked on.

  Next, the results of the A/B experiment, divided by user behavior, were analyzed and the hypothesis about the equality of conversion to contract views was tested.


**First test:**
- Some users perform actions with `tips_show` and `tips_click`,
- Others only with `tips_show`.

**Hypothesis**: Conversion to contact views differs between the two groups.

**Second test:**
- Some users perform actions using `favorites_add`,
- Others without using `favorites_add`.

**Hypothesis**: Conversion to contact views differs between the two groups.

A/B tests conducted revealed statistically significant differences between the groups.
Those. the use of additional actions `tips_click` and `favorites_add` affects the conversion of users to the target action.
