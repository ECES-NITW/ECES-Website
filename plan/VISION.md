# ECES Website

## 1. Core Principles 
- Component-first development. No page-specific hacks. Everything must be reusable.

- Data-driven content. Events, members, projects, and resources are updated via structured data files, not JSX edits.
- Clear ownership. Every part of the site has a responsible owner.
- SOP-driven updates. Anyone following the SOP should be able to update the site safely.

## 2. Website Structure
Navigation Bar (fixed for now)
- Home
- Team
- Events
- Projects
- Resources

## 3. Repo Structure 
```
ece-website/
├─ src/
│  ├─ components/        # Reusable UI components 
│  ├─ pages/             # Page-level composition using components
│  ├─ data/              # JSON data for content updates
│  │   ├─ team.json
│  │   ├─ events.json
│  │   ├─ projects.json
│  │   └─ resources.json
│  ├─ lib/               # Helpers, constants, utilities
│  └─ styles/            # Global styles / tailwind config
│
├─ public/
│  ├─ team/
│  ├─ events/
│  ├─ projects/
│
├─ SOP/                  # Step-by-step instructions for updates
├─ docs/                 # Architecture, design, decisions
├─ README.md
└─ ARCHITECTURE.md
```

## 4. Section-wise Requirements & Deliverables
### 4.1 Team

Data Source: ```src/data/team.json``` \
Assets: ```public/team/```

Required Fields
```
{
  "name": "",
  "photo": "",
  "position": "",
  "linkedin": "",
  "github": ""
}
```

### Deliverables
- Reusable MemberCard component
- Grid-based Team page
- Ordered by hierarchy 

### Responsibility

- Content: Content Lead
- UI: Design Lead
- Component: Dev Lead

---

### 4.2 Events

Data Source: ```src/data/events.json``` \
Assets: ```public/events/```

Required Fields
```
{
  "title": "",
  "date": "",
  "venue": "",
  "description": "",
  "images": []
}
```

### Deliverables

- Event listing page
- Reusable EventCard component

### Responsibility

- Data updates: Content Lead
- Page logic: Dev Lead
- Visuals: Design Lead

---

### 4.3 Projects

Data Source: ```src/data/projects.json``` \
Assets: ```public/projects/``` 

Required Fields
```
{
  "title": "",
  "images": [],
  "description": "",
  "link": "" # If applicable
}
```

### Deliverables

- Project cards
- External link support
- Responsive layout

### Responsibility

- UI: Design Lead
- Implementation: Dev Lead

---

### 4.4 Resources

Data Source: ```src/data/resources.json```

Required Fields
```
{
  "year": "",
  "subject": "",
  "link": ""
}
```

### Deliverables

- Filterable list (by year / subject)
- Clean, readable layout

### Responsibility

- Data: Content Manager
- Page logic: Dev Lead

---

## 5. Design System

### Design decisions must be consistent and documented.
- Colors
- Font scale
- Spacing
- Border radius
- Shadows

Documented in:
```docs/DESIGN_TOKENS.md```

---

### Core Components (Mandatory)

- Navbar
- Hero
- EventCard
- MemberCard
- ProjectCard
- SectionHeader
- Footer

### Each component must:

- Be reusable
- Accept props
- Have no hardcoded content
- Be documented

---

## 6. How Work Is Allocated
### Component Development
- Each student owns 1–2 components
- One component = one PR
- No massive PRs

### Page Development

- Pages are assembled only after components are approved
- No inline CSS hacks

### Content Updates

- JSON-only changes
- No JSX edits
- Must follow SOPs

## 7. Contribution Workflow (Mandatory)
```
1. Create a branch
2. Complete ONE logical task
3. Open PR with clear title
4. Reviewer checks:
   - Design consistency
   - Component reuse
   - Data-driven logic
5. Merge only after approval
```


## 8. SOP-Driven Updates

All repeatable actions must have SOPs inside ```/SOP```.

### Mandatory SOPs:

- ```ADD_EVENT.md```

- ```UPDATE_TEAM.md```

- ```ADD_PROJECT.md```

- ```ADD_RESOURCE.md```
