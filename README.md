# Technical Assessment
*If you have questions, please contact your recruiter via email.*

## Introduction
At GovPro AI, we work with a variety of web technologies, integrating multi-faceted data to create stable, high-value applications. This assessment is meant to test for those skills.

While building GovPro AI, we built a strong foundation of document processors that can parse information from documents and surface the data in clean user interfaces. For this task, we'd like you to **build a simple frontend to allow us to highlight sentences in a document.**

## The Task
A popular platform in the government contracting space is SAM.gov (which used to be called FedBizOpps) and hosts RFPs, RFIs and other solicitation documents from federal agencies stating their requirements for government contractors to bid on their jobs. However, it's a big awkward database and difficult to extract information from, and most resort to parsing out documents.

A common task is to go through a document from SAM and highlight important sentences. We'd like you to build a frontend tool that displays a PDF or Word file and allows the user to highlight sentences by simply clicking on them (**NOT clicking and dragging to highlight**). The user should be able to mouse over sentences and click any word to highlight the entire sentence. If a document is already highlighted in Yellow, it should pick a different color for any new highlights.

For PDFs, we'd like you to use examples of solicitation documents found on SAM -- please see attached samples to get you started.

## Requirements
Just 3 requirements: 

  1. Parse a PDF or Word document sentence by sentence (there are many ways to do this, e.g. PDF.js)
  2. Render the document in the frontend of your app, with sentences inline and intact as part of a paragraph.
  3. Clicking on a word in your frontend should highlight the entire sentence that the word is in.

**It is highly suggested to include either comments or a README writeup detailing any design choices you made.**

## Limitations
- You MUST use TypeScript (no JavaScript, you may utilize WASM if needed)
- We prefer if you build your application purely in the frontend. If you require a backend you MUST keep it in TypeScript as that is paramount to the assessment.
- You MUST use Vue.js, specifically Vue 3
- You may use any existing library but it MUST be open source, MIT licensed

Your solution can be a single page (SPA), or multiple pages.
Extra points will be issued for use of the Composition API and Single File Components (SFCs).

## Directions
  1. Create a private GitHub repository. It must be on GitHub, and it must be private (this is free)
  2. Build a solution (this is designed to take less than 2 hours, please see the assessment section below).
  3. Optional but HIGHLY SUGGESTED: write up any design choices you made.
  4. Add 2 collaborators: `govproai` and `cuuupid` ([How to Add Collaborators to a GitHub repo]([url](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository))
  5. Email us with a link to your repo so we know you're submitting your solution :)

## Assessment
We have a very transparent method by which we assess solutions, which you can find below. Solutions are marked out of 100.

Important: the design of your solution is an equally important aspect beyond completion. This assessment is designed to take NO LONGER THAN 2 HOURS. If you need to make compromises, reduce functionality, etc please note that in either a comment or a README. We award generous amounts of partial credit if you fall short in any aspect below but give an explanation as to why.

- **Completion (40 points):**
    - **Building a solution** (10 points)
    - **Meeting the requirements** (30 points, 10 for each requirement)
    - **Not breaking any limitations** (penalty, -10 for each limitation broken)
- **System Design (20 points):**
    - It is highly suggested to include either comments or a README writeup detailing design choices. This will help us award credit for design decisions.
    - **Extensibility (10 points)**, can this solution deal with more documents or document data in the future? Does it create technical debt?
    - **Tooling (5 points)**, did you decide on a pure frontend or frontend-backend pair? Did you build a SPA or use different pages? What frameworks or tools did you use?
    - **Code Style (5 points)**, this isn't about tabs/spaces, this concerns using modern syntax, good design patterns in your code, efficient and safe choices, e.g. const and let instead of var, or async methods, or where computations live
    - **Composition API (10 points**, did you use the Vue 3 Composition API and Single File Components (SFCs)?
- **User Experience (20 points)**
    - Intuitive interface (5 points), a member of our UX team will do a blind review
    - Styling (5 points), if there are no CSS artifacts and the page looks somewhat modernly styled you'll get full marks
- **Stability (10 points)**
    - **We can run the solution (5 points)**, if it requires a special command please make it clear in the README
    - **It keeps working when we change the underlying document (5 points)**
- **Speed (10 points), measured in time taken until page is interactive**
    - This is only 10 points, please keep this in mind and do not over-optimize
    - We will measure from the time we start loading the page until the time we can click a word and highlight a sentence
    - Solutions interactive in 11 seconds will net 1 point.
    - Each second reduced will net an additional 1 point.
    - Solutions that are interactive in under 2 seconds will net 10 points, which is the maximum score.
    - If you have a backend, we will not count startup time

Solutions that allow exporting data from the frontend (e.g. a JSON array of highlighted sentences) will net an extra 10 points.
