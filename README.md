# Current Events Warmup Generator

A single-page web app that turns current news headlines into printable classroom warmups across multiple secondary subjects.

The project is built around a simple instructional idea: students are more likely to engage when work feels relevant, and classes tend to run more smoothly when they begin with a predictable opening routine.

This prototype helps reduce the daily friction between current events, skill practice, and classroom structure.

## What It Does

The app generates short, printable warmups anchored in current headlines.

Each warmup includes:

- A short description of the news event anchoring the exercise
- The subject and skill being practiced
- A brief explanation of why the skill is relevant to the event
- A student-facing problem
- A button that reveals the answer
- A formula box when a science or math task requires one

The app supports both automatic headline loading from public RSS-style sources and manual headline entry.

## Supported Subjects

The current version includes warmups for:

- Algebra 1
- Geometry
- Algebra 2
- High School English
- World History
- Civics
- Psychology
- US History
- Government
- Health
- Life Science / Middle School Biology
- Biology / High School Biology
- Physical Science / Middle School Physics
- Physics / High School Physics

Users can generate one subject at a time, subject sets, or all subjects at once.

## Why This Matters

Many teachers want to connect classwork to the real world, but creating relevant warmups every day takes time.

A teacher has to:

1. Find a usable current event
2. Decide whether it is appropriate for students
3. Match the event to a skill
4. Write the prompt
5. Check the answer
6. Format it for classroom use

That workflow is valuable, but it is difficult to repeat every morning.

This app explores how a lightweight AI-adjacent workflow can help turn current information into structured, skill-aligned classroom routines.

## Moral Filter

The app includes a moral filter for tragedy-sensitive headlines.

Some current events should not be turned into calculation exercises. For example, a headline about a shooting should not produce a physics problem about bullet speed, force, energy, or rate of fire.

The moral filter detects sensitive topics such as:

- Shootings
- Violence
- Deaths or injuries
- War or attacks
- Abuse
- Suicide
- Disasters
- Crashes
- Weapons

When a headline is flagged, the app redirects the warmup away from quantifying harm. Instead, it uses safer tasks such as:

- Responsible language
- Evidence evaluation
- Ethical variable selection
- Institutional response
- Public communication
- Support and prevention framing

The purpose is not to avoid difficult topics entirely. The purpose is to avoid turning human harm into a decontextualized academic exercise.

## Design Goals

This project is designed to be:

- Fast enough for daily classroom use
- Printable
- Easy to adapt
- Usable without requiring a login
- Safe enough to handle sensitive headlines more responsibly
- Structured around skills rather than generic discussion prompts
- Flexible across multiple subjects

## How to Use

Open the app in a browser.

Then choose one of the following options:

1. Select a subject or subject set from the dropdown menu.
2. Load headlines automatically, or paste your own headlines manually.
3. Generate the warmups.
4. Print the page or use it digitally.
5. Click **Show answer** when ready to reveal the solution or sample response.

## Manual Headline Mode

If headline feeds are unavailable or blocked, users can paste headlines directly into the app.

This is useful when:

- A school network blocks news feeds
- A teacher wants to use specific local headlines
- A teacher wants to avoid a particular story
- A teacher wants more control over the content students see

## Agent Mode

The app can also be accessed with headlines passed through the URL.

Example:

```text
index.html?headlines=headline one|headline two|headline three
```

A subject can also be specified:

```text
index.html?headlines=headline one|headline two&subject=algebra-1
```

This makes the app easier to use with a future AI agent or automated workflow.

## Technical Notes

This is a single-page HTML, CSS, and JavaScript prototype.

It does not require a backend server.

It does not store an AI API key in browser code. That is intentional. API keys should not be exposed in public client-side code.

The current version uses deterministic templates, headline classification, topic-sensitive variation, and safety filtering rather than live AI generation inside the browser.

## Possible Future Improvements

Future versions could include:

- A server-side AI generation layer
- Teacher-controlled grade level settings
- State standard tagging
- Saved warmup history
- Local news source selection
- Better headline source configuration
- Export to Google Docs or PDF
- Teacher review mode before printing
- More nuanced topic sensitivity controls
- Differentiated versions of the same warmup

## Project Status

Prototype.

The app is functional, but it is intended as a starting point for exploring current-events-based warmup generation, classroom workflow design, and safe AI-assisted instructional routines.

## License

Choose a license before publishing publicly.

MIT is a reasonable option if the goal is to allow others to reuse and adapt the project.
