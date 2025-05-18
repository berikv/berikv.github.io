---
layout: post
author: Berik
date: 2025-03-22 14:30:00 +0200
title: Handling Software Errors Effectively
abstract: Learn how distinguishing between user-caused and system-caused errors improves your app's reliability and usability.
categories: Programming
published: false
---

## Handling software errors

Does your app have messy error handling? Do users report the app is difficult to use?
Doing a deep-dive on error handling may help you out!

To help form a framework for error handling we need to define what valid-use is.

**Valid use** is any predictable interaction within normal user expectations. Invalid use involves deliberate or unpredictable interactions outside the intended application design.

Identifying whether errors result from valid or invalid usage informs the best approach for resolution—whether improving UX, clarifying instructions, or enhancing resilience against misuse.

To nail this down, this is an extensive list of operations considered valid-use:

* Clicking / tapping / swiping anywhere in / on the site / app
* Pressing any key on the keyboard
* Using common keyboard shortcuts like ctrl+c ctrl+v etc
* Using context buttons like the browser back / forward buttons, or the Android back button
* Adjust the url in the navigation bar of their browser
* Any action the user is told is possible (eg: ctrl+k to search, swipe up to refresh)
* Other operations that given the context are valid user behaviours, eg: disconnecting the internet, etc
* Any combination of the above actions

Examples of invalid-use operations include:

* Clicking extremely fast
* Entering an extreme amount of text
* Opening developer tools or a decompiler and adjusting the source code
* Installing a proxy or browser plugin and adjusting request / response data

Users performing invalid-use operations aren’t guaranteed user-friendly error messages.

Is the error condition a direct result of valid-use? Then you're dealing with a **usage error**.

> The definition of what constitutes valid use has some flexibility. Depending on the
> context you may want to use a different definition. Keep in mind that the more user behaviour
> is considered valid-use, the more work you have to do as a developer, and the more the user
> expenience can be improved.

### Usage error - an example

Date entry is notoriously difficult. Not only does the user need to type a combination of numbers and characters in a specific ordering, the numbers also mean different things depending on the locale. Does your application require "31/12/2025" or "2025-12-31" as a date format?

A user who inputs "12/31/2025" in an input field which requires "dd/mm/yyyy" as the date format, causes a usage error.

There are different ways of handling usage errors. These are some common ones:

* Return a "500 internal server error" or crash the app

  This may be very convenient for the developer, and safe for the application, but is very user unfriendly.

* Show an in-context and actionable error message

  eg: *Please enter a date in "dd/mm/yyyy" format* or *Choose a date in the future to plan an appointment* -- next to the input field where the fault occurs. This way the user is less likely to lose track of what is going on

* Adjust the user interface more fundamentally
  
  eg: Use a date-picker component instead of a text input for date input. This requires most developer work: design must be adjusted, a date-picker comonpent must configured. On the other hand, this solution is very user friendly. It even solves the date format locale issue completely.

Q: Can I use data driven desicion making?

A: Yes. Use funnel analysis to establish which usage errors to tackle first.

### System errors

System errors can not be solved solely by improving the UX.

A great way to start reducing system errors is by adding application logs.
Make sure logs include sufficient context—such as request URLs and user IDs. Make sure to log edge-cases to simplify debugging.
Familiarise yourself with the log contents before an outage happens, so that you are not surprised with something trivial.

Add enough context in the log, eg the request urls. Add logs for edge cases.

While UX can't solve system errors, UX does matter.
If system errors are common or damaging, add a friendly message.
If there is a system wide outage, communicate the status of the outage.
Follow up with your users after the outage with information and a plan for mitigation.

## Conclusion

By first covering wether errors are due to valid use or not, we can quickly focus on the right
strategy to improve the system.

Distinguishing between usage and system errors helps you focus your efforts. Usage errors signal opportunities for UX improvements. System errors point to potential infrastructure / resilience improvements. By systematically analyzing errors through this lens, you can continuously improve user experience and application reliability.
