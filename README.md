# Home Base

Home Base is a personal desktop dashboard that pulls my calendar, coursework due dates, unread email and recent Google Drive files into one screen. It connects to Google Calendar, Gmail and Drive with read-only access, so it never sends email, changes events or edits files. Everything runs locally: Google data comes straight to my computer, and my tasks, budget entries and trackers are stored only on that machine. I built it with Claude Code for my own use, so it isn’t available to download or sign up for.

This repository doesn't contain the app's source code. It hosts the app's [homepage](https://lukepolich.github.io/homebase/) and [privacy policy](https://lukepolich.github.io/homebase/privacy.html).

## Features

### Widgets
Each section of the dashboard is a widget that can be shown or hidden.

- **Next 7 days:** upcoming events from Google Calendar, grouped by day, with what's happening now highlighted. You choose which calendars appear.
- **Coursework:** assignments and due dates from a Canvas calendar feed, flagged when they're due soon or overdue. You can check them off as you turn them in.
- **To do:** a task list with optional due dates.
- **Unread mail:** the latest unread messages in your Gmail Primary inbox.
- **Recent files:** the Google Drive files you opened most recently.
- **Budget:** a monthly budget with spending by category, and a pace marker that shows whether you're on track for the month.
- **Portfolio:** tracks stock, ETF and crypto holdings with live prices. It has a value chart over 1 day to 5 years and per-holding stats like day range and 52-week range.
- **Daily trackers:** log anything daily, like sleep, workouts, study hours or water. Each tracker has a 14-day chart, goals and streaks.
- **Summary bar:** the next event, coursework due, open tasks, budget left and unread mail, all in one row.

### Tabs
Besides the Home page, you can create your own tabs, for a class, a hobby, money or anything else. Each tab has its own set of widgets, and it can be tied to one class (so it shows only that class's assignments) and to particular calendars. Tasks you add on a tab stay on that tab, while Home shows everything.

### Focus mode
Press **F** to hide everything and pick one task or assignment to work on. It shows large, along with how long you've been on it and your next calendar event, so you don't miss a class. You choose which widgets, if any, stay visible.

### Time and weather
The current temperature and time sit at the top of the screen. Both follow your location automatically, or a city you set, and the clock shows a time-zone label when you're somewhere else.

### Settings
- Themes: Navy, Dark, Light, or match Windows
- Accent colors, text size and layout density
- Reduce motion
- 12- or 24-hour clock, and °F or °C
- Which tab opens at startup, and how often data refreshes
- Backup export of your saved data

## How it's built

- **Desktop app:** Python with [pywebview](https://pywebview.flowrl.com/). The interface is HTML, CSS and JavaScript, shown in the Windows Edge WebView2 engine.
- **Google data:** the official Google Calendar, Gmail and Drive APIs, signed in with Google's standard sign-in and **read-only** permissions.
- **Coursework:** read from a Canvas calendar feed subscribed in Google Calendar.
- **Prices:** live and historical prices from Yahoo Finance's public chart data.
- **Weather:** [Open-Meteo](https://open-meteo.com/), plus an approximate location lookup based on your internet connection.
- **Storage:** everything you enter (tasks, budget, trackers, holdings, tabs and settings) is saved in a local file on your own computer.

## Privacy

- Home Base has no server. Data from Google goes straight to your computer and is shown on screen. It's never uploaded, sold or shared.
- Google access is read-only. Home Base can't send email, change calendar events, or edit or delete files.
- Your sign-in and everything you enter stay on your computer.

Read the full [privacy policy](https://lukepolich.github.io/homebase/privacy.html).
