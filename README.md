# Deadline Diary

An exam countdown and study tracker for students. Add your exams, see how many days are left, and tick off topics as you finish them.

Made for the Multidisciplinary Lab (post-lab practical) using HTML, Tailwind CSS and JavaScript.

## Why I made this

During exams I never know exactly how many days are left for each subject or what I still haven't covered. I wanted one simple page where I can see all of that at once, so I made this.

## Features

- Add an exam with a subject name and date
- Live countdown (days, hours, minutes, seconds) for the nearest upcoming exam
- Exam cards sorted by date, with a "days left" badge that changes colour as the exam gets closer
- Add study topics under each exam and tick them off
- Progress bar for every exam based on ticked topics
- Delete exams or topics
- Filter exams: All, Upcoming, Over
- Summary boxes showing total exams, tasks done and days to the next exam
- Form validation (empty subject, missing date or past date shows an error message)
- Responsive layout for mobile, tablet and laptop

## Tech used

- **HTML** for the page structure
- **Tailwind CSS** (via CDN) for styling and responsive design
- **JavaScript** (plain, no libraries) for the logic: DOM manipulation, events, arrays, functions, `Date` and `setInterval`
- **Google Fonts**: Bricolage Grotesque, DM Sans, IBM Plex Mono

## How to run

1. Download or clone this project.
2. Open `index.html` in any browser.

That's it. No installation needed. You just need an internet connection the first time so that Tailwind and the fonts can load.

## Project structure

```
deadline-diary/
  index.html    (HTML, CSS and JavaScript are all in this one file)
  README.md
```

## How it works

All the exams are stored in one array called `exams`. Every time something changes (adding an exam, ticking a task, deleting, changing the filter), the array is updated and the `render()` function redraws the cards on the page. The countdown at the top is refreshed every second using `setInterval()`.

Some of the main functions:

| Function | What it does |
|---|---|
| `addExam()` | Validates the form and adds a new exam |
| `addTask()` | Adds a topic under an exam |
| `toggleTask()` | Marks a topic as done or not done |
| `getDaysLeft()` | Finds how many days are left for an exam |
| `getUrgencyClass()` | Picks the badge colour based on days left |
| `render()` | Sorts, filters and draws all the exam cards |
| `updateCountdown()` | Updates the live countdown every second |

## Colour meaning

- Red badge: 3 days or less
- Yellow badge: 4 to 7 days
- Blue badge: more than 7 days
- Grey badge: exam is over

## Responsive design

The layout is mobile-first. Exam cards show in 1 column on phones, 2 columns on tablets and 3 columns on laptops, using Tailwind's `sm:`, `md:` and `lg:` classes.

## Limitations

- Data is not saved. If you refresh the page, it goes back to the sample exams.
- The exam time is fixed at 9:00 AM for the countdown.

## Future improvements

- Save data using `localStorage` so it stays after refresh
- Let the user set the exam time
- Add a dark mode
- Turn this into a full attendance and bunk calculator

## Author

YOUR NAME
B.Tech Computer Science and Engineering, S.B. Jain Institute of Technology, Management & Research, Nagpur
