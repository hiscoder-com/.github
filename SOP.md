<div id="top"></div>
<br />
<div align="center">
<h1 align="center">SOP - SoftWare Development</h1>
</div>

Source Control.

All workflows go through GitHub, where a project with several task boards is created to manage the process. This helps organize the work of the team, including developers, designers, and testers.

Main columns:
- **TODO** - a general list of tasks.
- **Sprint** - tasks planned for the current sprint.
- **In progress** - tasks that are currently being completed.
- **In check** - tasks being checked.
- **Done** - completed tasks.
- **Blocked** - tasks blocked due to dependencies on other tasks.

Task parameters:
- **Team** - team or task type (UI/UX, Design, Programming, Testing).
- **Priority** - priority (High, Medium, Low).
- **Size** - task size (XS, S, M, L, XL).
- **Estimate** - estimated completion time.
- **Sprint** - assigned sprint.
- **Start date** - start date
- **End date** - end date

<h2 align="center">Preparing for the sprint</h2>
New tasks are added to the TODO column.
If the task is too large, it should be broken down into several smaller tasks, each of which should be completed in a week or less.
Tasks for the sprint are moved to the Sprint column, distributing them among team members.
<br>
<h4 align="center">Creating a task</h4>

Creating a task:

- **Title** - a short description starting with a tag, such as `[Design]-`, `[UI/UX]-`, `[Feature]-`, or `[Testing]-`.
- **Task description** - a detailed description of the task.
- **Evaluation criteria** - measurable results by which to evaluate the task's completion.

Additional attributes:

- Examples and links to code or solutions.
- Links to mockups.
- Additional information, screenshots, and steps to reproduce the error (if it is a bug).

<br>
<h2 align="center">Developer's work</h2>

1. Getting started:

- Check your assigned **Pull Request** or tasks - they are in priority.
- Select a task from the **Sprint** column.
- Make sure the task is clearly described and understandable.
- Move it to **In progress**.

2. Work on the task:

- Describe the plan for completing the task as **General solution** and **Implementation steps**, then confirm them with the manager.
- Create a new branch from the current working branch (usually **develop**).
- Commit small changes with clear messages.
- Create a **Pull Request (PR)** associated with the task.

3. Review and close:
- When creating a **PR**, you must briefly describe the work done in **Description**
- When creating a **PR**, the card is automatically moved to **In check**
- Perform a manual code review to ensure there are no simple errors such as left-over comments and console.log()
- Assign at least two reviewers to your **PR** and notify them.
- When you get two approvals, merge the branches into **develop**.
- Delete the working branch after merging.
- Release to **master** at the end of the sprint.
<br>
<h4 align="center">Blocks and conflicts</h4>
- If you encounter a problem or dependency, review the task plan and consult documentation or other sources.
- If a task is blocked by another task, contact the assignee of the blocking task and note its number in the description of your task. Move your task to Blocked.
- If there are unblocked tasks, continue working on them or request new tasks from the manager.
<br>
<h4 align="center">Correct branch naming</h4>
<br>

`{type}-{name}-{number}`
<br>
where **type** is the branch type (feature, fix)
**name** is the nickname of the developer working on the branch
**number** is the number of the attached GitHub issue

Example: `feature-john-34`.

If several developers are working on the branch, the nickname is not specified (e.g. `feature-34`).
<br>

<h2 align="center">How to fix bugs</h2>

- Make sure the steps to reproduce the bug are clear.
- For critical bugs, create a **hotfix** branch from **master**, then merge the changes into master and develop.
- For non-critical bugs, follow the normal workflow.

<h2 align="center">Checking a Pull Request (PR)</h2>

- Make sure there are no unnecessary comments or console.log() in the code.
- Update the Changelog and version in package.json.
- Follow the coding standard (see the Codestyle section).
- If there are UI/UX changes, update the documentation and screenshots.
<h2 id="sermver" align="center">Semantic Versioning (SemVer)</h2>
Versions consist of three parts: {major}.{minor}.{patch}:

- major — changes that are incompatible with previous versions.
- minor — adding new functionality that does not break compatibility.
- patch — bug fixes without changing functionality.
Read more at semver.org.
<br>
<h2 id="changelog" align="center">Project Changelog (Changelog)</h2>
<br>
