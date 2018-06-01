# README: Jareds Power Calendar
This is a calendar for power users. It includes advanced features like commute planning, mass editing, cli-support, and more. It can be both locally hosted or accessed on a server.

## To-Do:
- Find a better name for it
- Create a database for 

## Structure:
- Database to hold information about the calendar
- Web UI
- Command-Line support (both as a static command or interactive mode which mimics the web UI)
    - Static command line can be used within scripts. 
    - What this might look like: "powcal -A -n 'Lunch with friends' -t '12:30PM' -d '2018-06-04'"

## Features:
- Weather import from various services
- Events
    - Events can have a location associated with them.
    - Location data will be used to calculate commute times between events
    - Commute-time data will be taken from Google Maps or OpenStreetMaps, not sure yet, maybe I'll provide the option to choose.
    - Extra fields for plugins
- To-Dos
    - Have a priority, time-to-complete, and difficulty associated with them.
    - Can automatically be dispersed throughout the calendar using that information.
    - Settings for auto-dispersial can be changed (including default time between tasks, break times, best time of day for difficult tasks, etc.)
    - Several types of To-Dos that can be nested:
        - Projects
        - Tasks
        - Subtasks
    - To-Dos can be tagged for different categories (such as school, work, other activities, etc.)
    - Optional reminders for the halfway point (from creation), x days before, and a formula-controled time based on both the difficulty and anticipated time-to-complete
    - Extra fields for plugins
- Calendar import/sync
    - Can import & sync data from Google Calendar, Cozi, and anything iCal format.
    - Will allow you to change events from other calendars locally. If there's a conflict (for example, you change the event time on your calendar, but someone changes it on the source calendar), it will inform you and allow you to adjust what's necessary. - Not sure if this is possible yet.
- Plugin support
    - School plugin
        - Event type for classes
        - To-Dos associated with classes
        - Rotating schedules and what not
    - Sleep-Schedule plugin
        - Templates for sleep schedules
        - Warns you if your waking or sleeping times change too much day-to-day
    - Morning/Evening routine plugin
    - Advanced commute-time features for biking/walking:
        - Money-saved by biking or walking instead of driving
        - Commute-time can change for mode of transportation, and mode can change based on events intelligently (if the weather is nice enough for biking/walking and the distance isn't too far, it might suggest biking/walking instead)
        - Biking times can be adjusted based on fitness level (so if it takes you less time to bike than average, you can adjust accordingly)
        - Biking times would take into account average set-up time (to check your tires, load up, lock up your bike, etc.)
