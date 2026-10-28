# DSA Tracker :

A lightweight, browser-based **DSA problem tracker** for keeping track of interview preparation.

The tracker organizes problems across common data structures and algorithm topics, lets you mark problems as solved, and keeps personal notes and solution links alongside each problem.

## Features

* 📊 **Overall progress tracking**

  * Percentage completed
  * Problems solved
  * Problems remaining
  * Total problems

* 🗂️ **Topic-based organization**

  * Arrays & Strings
  * Hashing
  * Linked Lists
  * Stacks, Queues & Monotonic Structures
  * Recursion & Backtracking
  * Sorting
  * Binary Search
  * Trees & BSTs
  * Heaps / Priority Queues
  * Graphs
  * Dynamic Programming
  * Greedy
  * Bit Manipulation
  * Math & Number Theory
  * Design Problems
  * Advanced / Differentiator Tier

* 🔎 **Search**

  * Quickly find problems by name.

* 🎯 **Filtering**

  * All problems
  * Solved problems
  * Unsolved problems

* 📝 **Problem notes**

  * Add your approach
  * Record mistakes and edge cases
  * Write down things that tripped you up

* 🔗 **Solution links**

  * Store a GitHub solution link for each problem.
  * Open the solution directly from the tracker.

* 📈 **Per-topic progress**

  * Each section displays its own solved/total count.
  * Progress bars show completion for each topic.

* 💾 **Persistent progress**

  * Progress, notes, and solution links are saved using the browser's `localStorage`.
  * Data survives page refreshes and closing/reopening the browser.

## Tech Stack

This is intentionally a very small project with no framework or backend.

* **HTML**
* **CSS**
* **Vanilla JavaScript**
* **Browser LocalStorage**

Everything lives in a single HTML file.

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd dsaTracker
```

### 2. Open the tracker

Simply open:

```text
dsa_tracker.html
```

in your browser.

That's it.

There is:

* No Node.js
* No Python
* No database
* No build process
* No dependencies

## How It Works

Each problem gets a unique key based on its section, problem name, and position in the list.

The tracker stores an object containing information such as:

```javascript
{
  done: true,
  note: "Used sliding window + hashmap",
  link: "https://github.com/username/dsa-solutions/..."
}
```

The complete progress object is serialized and stored in:

```javascript
localStorage
```

When the application starts, it loads the saved data and renders the tracker with your previous progress.

## Data Persistence

Your data is stored locally in the browser.

This means:

```text
Solve problem
     ↓
Update progress
     ↓
Save to localStorage
     ↓
Close browser
     ↓
Open tracker again
     ↓
Progress restored
```

### Important

The data is tied to the browser/device where you use the tracker.

It does **not** currently sync between:

* Different browsers
* Different computers
* Different users

If you want cloud synchronization, the project could be extended with a backend and database.

## Project Structure

The project is intentionally minimal:

```text
dsaTracker/
│
├── dsa_tracker.html
└── README.md
```

The HTML file contains:

```text
HTML
├── UI structure
├── CSS styling
└── JavaScript
    ├── Problem dataset
    ├── State management
    ├── Search/filtering
    ├── Progress calculations
    ├── Notes & links
    └── LocalStorage persistence
```

## Problem Coverage

The tracker contains problems spanning the major DSA areas needed for technical interview preparation, including trees, graphs, dynamic programming, binary search, greedy algorithms, heaps, linked lists, backtracking, and more.

The problem set is organized around interview-preparation resources such as **NeetCode 150** and **Striver's A2Z sheet**, as described in the application itself.

## Future Improvements

Some things that could be added later:

* [ ] Cloud synchronization
* [ ] User accounts
* [ ] Firebase / Supabase backend
* [ ] Import/export progress as JSON
* [ ] Daily problem goals
* [ ] Streak tracking
* [ ] Difficulty labels
* [ ] LeetCode links
* [ ] Spaced repetition / revision tracking
* [ ] Multiple study plans
* [ ] Analytics and progress history
* [ ] Mobile/PWA support

## Why I Built This

Most DSA trackers are either overloaded with features or tied to a particular platform.

This one is deliberately simple:

**Open it → solve problems → check them off → write down what you learned → keep going.**

No account. No setup. No dependencies.

Just a personal DSA progress tracker.

---

## License

This project is open source. Feel free to modify it and adapt it for your own interview preparation.
