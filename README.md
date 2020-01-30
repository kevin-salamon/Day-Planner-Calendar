# Day-Planner-Calendar
A color-coded day planner that will allow you to save and track events throughout the normal workday.

Overall, the construction of this program is simple to follow. The columns and jumbotron container  which encloses all the data on the page is made with Bootstrap. Within the time-labeled columns, the user may write their daily plans and save this writing to the local storage by clicking the "lock" button attached to the right side of each respective row. 

The code that allows the saving of the written data to the local storage is simple DOM manipulation. Individual time-slot columns are targeted by their respective row 'lock' button, in which the clicking of same will trigger the local storage.

The columns are colored according a comparison with the current hour - if the time-slot is in the past, it will be colored grey; present (within the same hour) will be red, and future time-slots will be green. This comparison is done using values assigned directly within the html time slots, equivalent to the military time of the slot (i.e. 9:00 AM will equal 9, 2:00 PM will equal 14, etc.). JQuery can call this value and assign it to a variable. The current time (in hours) will then be declared via moments.js function moment().hours(). Then, again using JQuery, we can compare these two values directly, and assign classes to the respective elements based on this comparison. These classes (past, present, future), will then color the proper time-slots based on the current hour.
