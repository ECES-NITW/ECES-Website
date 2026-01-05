# implementation timeline (tentative)

## Phase 0: kickoff and alignment  
**jan 5 – jan 6**

### People required
- minimum 4 to 6 contributors

### Objectives
- align everyone on what is being built
- remove ambiguity early
- freeze fundamentals

### Tasks
- read and agree on:
  - `VISION.md`
  - `PROCEDURE.md`
- confirm:
  - navigation structure is final
  - repo structure is final
  - data-driven approach is mandatory
- clarify expectations:
  - no direct pushes to main
  - no skipping reviews
  - no undocumented changes

### Deliverables
- shared agreement on scope and rules
- no open debates on stack or structure

### Exit condition
everyone understands how work will flow and what “done” means.

---

## Phase 1: architecture and repo setup  
**jan 7 – jan 9**

### People required
- 2 to 3 contributors

### Objectives
- create a stable technical base
- ensure the project builds cleanly from day one

### Tasks
- initialize repository with final folder structure
- add placeholder files:
  - `ARCHITECTURE.md`
  - empty json files in `src/data`
- verify:
  - local dev server runs
  - production build succeeds

### Deliverables
- working repo
- frozen folder structure
- documented architecture decisions

### Exit condition
any contributor can clone the repo and run it without help.

---

## Phase 2: design tokens and component specification  
**jan 10 – jan 14**

### People required
- 2 to 3 contributors

### Objectives
- define the visual identity once
- prevent ui inconsistency later

### Tasks
- finalize:
  - color palette
  - font scale
  - spacing system
  - border radius and shadows
- define component contracts:
  - props
  - variants
  - intended usage
- write `docs/DESIGN_TOKENS.md`

### Deliverables
- locked design tokens
- finalized component list
- no ambiguity about look and feel

### Exit condition
components can be built without design guesswork.

---

## phase 3: Core component development  
**jan 15 – jan 21**

### People required
- 4 to 6 contributors

### Objectives
- build the reusable ui foundation
- avoid page-specific logic

### Tasks
build the following components only:
- navbar
- hero
- section header
- event card
- member card
- project card
- footer

rules:
- one component per branch
- one component per pr
- props only, no hardcoded content
- responsive by default

### Deliverables
- complete `src/components` directory
- reviewed and approved components

### Exit condition
all components are reusable and ready to be composed into pages.

---

## Midsem break  
**jan 22 – feb 7**

---

## Phase 4: pages and data wiring  
**feb 8 – feb 14**

### people required
- 3 to 4 contributors

### Objectives
- assemble pages using existing components
- enforce data-driven rendering

### tasks
create pages:
- home
- team
- events
- projects
- resources

rules:
- pages only compose components
- content must come from json files
- no inline hacks or quick fixes

### deliverables
- all pages render correctly
- json data drives all content

### Exit condition
updating json changes the site without touching jsx.

---

## phase 5: SOP writing and validation  
**feb 15 – feb 19**

### people required
- 2 to 3 contributors

### objectives
- make the site maintainable by future batches
- remove dependence on original developers

### tasks
write and test:
- `SOP/ADD_EVENT.md`
- `SOP/UPDATE_TEAM.md`
- `SOP/ADD_PROJECT.md`
- `SOP/ADD_RESOURCE.md`

validation:
- someone unfamiliar follows the sop
- no verbal explanation allowed

### deliverables
- complete sop folder
- tested, clear instructions

### exit condition
anyone can safely update the site by following docs only.

---

## phase 6: polish, qa, and release  
**feb 20 – feb 26**

### people required
- anyone available

### objectives
- stabilize and finalize v1
- ensure professional quality

### tasks
- mobile responsiveness
- basic accessibility checks
- cleanup docs and readme
- final review of repo

### deliverables
- stable main branch
- tagged v1.0 release
- handover-ready repository

### exit condition
the site can be passed to the next batch without explanation.

---
