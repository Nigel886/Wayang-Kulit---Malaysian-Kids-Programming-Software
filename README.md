# Wayang Kulit Coding Quest

## 1. Project Background

**Wayang Kulit Coding Quest** is a Human-Computer Interaction group project that explores how a culturally grounded mobile interface can support early Computational Thinking learning for children aged **7-11**.

The project was developed as a **high-fidelity interactive prototype** rather than a full production learning platform. Its primary purpose is to demonstrate how interface design, interaction flow, visual feedback, and pedagogical scaffolding can be combined in a single mobile experience for academic evaluation.

The prototype adopts a Malaysian **Wayang Kulit** theme and places the learning task inside a theatrical narrative in which the user helps Hanuman move across a five-step stage, avoid an obstacle, and reach a goal star by arranging logic blocks in the correct order.

---

## 2. Problem Statement

Young children often struggle with abstract programming concepts because digital instructions are invisible, spatial consequences are unclear, and error feedback is not always easy to interpret. In many beginner coding interfaces, children are required to infer movement, sequencing, and repetition without sufficient visual grounding.

This project addresses that issue by designing a mobile-first guided puzzle interface that makes computational actions visible, tangible, and culturally meaningful.

The prototype specifically investigates how:

- a **spatially mapped stage**
- **large manipulable coding blocks**
- **clear runtime animation**
- **error-preventive constraints**
- and **annotated HCI rationale**

can improve learnability and usability for a child audience.

---

## 3. Project Objectives

The main objective of this project is to design and implement an educational interface that introduces basic computational thinking concepts through a child-friendly interaction model.

### Learning objectives

- teach **sequence** through ordered action blocks
- teach **iteration** through the **Gamelan Beat** loop container
- teach **goal-oriented planning** through obstacle avoidance and end-state completion
- reinforce **cause-and-effect understanding** through animated stage feedback

### HCI objectives

- reduce the **Gulf of Execution** through familiar and constrained interaction patterns
- reduce the **Gulf of Evaluation** through explicit animation and error messages
- support child motor skills through large targets and guided placement
- maintain high visual engagement through gamified feedback and culturally localized aesthetics

---

## 4. Target Users

### Primary users

- Malaysian children aged **7-11** who are new to basic coding concepts

### Secondary users

- lecturers assessing the project under an HCI rubric
- peers reviewing usability, interaction design, and front-end implementation

---

## 5. Concept and Design Theme

The prototype is themed around **Wayang Kulit**, a traditional form of shadow puppetry in Malaysia. This cultural direction was selected to differentiate the project from generic coding interfaces and to create a stronger local identity.

The visual and interaction language incorporates:

- a puppet theatre style **Shadow Stage**
- batik-inspired decorative textures
- traditional metaphors such as **Tok Dalang**, **Kris**, and **Gamelan Beat**
- warm theatrical lighting and vivid gradients
- child-friendly rounded forms, thick borders, and animated visual rewards

The final result aims to balance:

- educational clarity
- cultural relevance
- playfulness
- academic explainability

---

## 6. System Overview

The system is presented in a strict **vertical mobile layout** inside an iPhone-style frame. The interface is divided into three major functional areas:

### 6.1 Shadow Stage

Located at the top of the screen, the stage provides immediate visual feedback for every action executed by the user.

Key stage elements:

- a visible **1x5 grid track**
- **Hanuman** as the controllable character
- a **Sacred Rock** obstacle positioned on Grid 3
- a glowing **goal star** on Grid 5
- an instructional subtitle banner that explains the current state

### 6.2 Script Canvas

Located in the middle of the interface, the Script Canvas is the area where the user assembles a sequence of blocks.

It supports:

- tap-to-append interaction
- drag-and-drop reordering
- visual insertion bars
- loop containment
- error highlighting

### 6.3 Block Palette

Located below the canvas, the palette provides the available logic blocks.

Available block types:

- **Move Forward**
- **Raise Kris**
- **Bow**
- **Gamelan Beat**

---

## 7. Computational Thinking Model

The prototype focuses on a small but meaningful set of computational thinking concepts.

### 7.1 Sequence

Children must arrange actions in the correct order. For example, **Move Forward** must appear before the character can progress across the stage.

### 7.2 Iteration

The **Gamelan Beat** block acts as a loop container. It allows repeated execution of its child blocks and makes the idea of repetition visible and concrete.

### 7.3 Conditional Planning

Although there is no explicit visual `if` statement block, the child must still understand that **Raise Kris** must occur before entering the obstacle cell. This encourages planning and prediction based on stage conditions.

### 7.4 Goal Completion

The task is not complete simply by reaching the final grid. The user must also finish with **Bow**, reinforcing the idea that successful programs often require both process completion and proper final state conditions.

---

## 8. Core Interaction Flow

The expected interaction flow is:

1. Observe the goal and obstacle on the stage
2. Select blocks from the palette
3. Build a sequence in the Script Canvas
4. Optionally place actions inside the **Gamelan Beat** loop
5. Press **Run**
6. Watch the stage animation execute step by step
7. Revise the sequence if an error occurs
8. Press **Reset** to restart testing

This interaction pattern is intentionally simple and repetitive so that children can focus on logic construction rather than interface complexity.

---

## 9. HCI Design Rationale

This prototype applies several core Human-Computer Interaction principles.

### 9.1 Visibility of System Status

- the stage banner narrates current action and progress
- Hanuman moves cell by cell rather than teleporting instantly
- success and failure states are shown immediately

### 9.2 Match Between System and the Real World

- the stage uses theatrical storytelling instead of abstract coding terminology
- **Raise Kris** functions like an intuitive power-up before a dangerous move
- **Gamelan Beat** expresses looping through a familiar cultural metaphor

### 9.3 Error Prevention

- sequence validation prevents clearly invalid block arrangements
- the loop boundary visually distinguishes “inside the loop” from “outside the loop”
- the **Bow** action is constrained to end-state logic

### 9.4 Recognition Rather Than Recall

- blocks are color-coded and icon-supported
- the 1x5 stage grid makes movement distance visible
- obstacle and goal remain visible during construction

### 9.5 User Control and Freedom

- users can drag, reorder, remove, and rebuild blocks
- Reset acts as an immediate recovery mechanism
- loop exit behavior allows children to continue the sequence outside the loop

### 9.6 Feedback and Gulf Reduction

- error states highlight the exact problematic block
- runtime text explains why failure happened
- animated movement reduces ambiguity in action interpretation

---

## 10. Academic Annotation Layer

To support coursework presentation and rubric-based evaluation, the interface includes a toggle labeled **Show Academic Annotations**.

When enabled, the prototype overlays formal annotation callouts that explain the HCI rationale behind specific interface components. These annotations are intended to support lecturer review and documentation screenshots.

The annotation layer covers:

- Familiar Schema
- Physical Constraints
- Motor Skill Support
- Tangible Iteration Metaphor
- Gulf of Evaluation support
- Menu discoverability

This feature is not only decorative; it explicitly bridges the working prototype with the academic discussion required in an HCI assignment.

---

## 11. Visual and Motion Design

The prototype adopts a bright, high-contrast, cartoon-like visual language in order to maintain child attention and reinforce game-like motivation.

Notable visual features include:

- vibrant gradients
- rounded child-friendly components
- animated stars and stage glow
- theatrical set dressing
- stylized block icons
- puppet micro-animation
- obstacle shatter particle effects

Motion is used not only for entertainment but also for feedback, instruction, and error explanation.

---

## 12. Runtime Logic Summary

The execution engine interprets the child’s script in a sequential asynchronous flow.

Key runtime behaviors:

- blocks are flattened into their executable order
- loop contents are expanded based on repetition count
- each action executes with controlled timing using `async/await`
- Hanuman moves one grid cell per movement action
- the obstacle can only be cleared when **Raise Kris** is active
- Reset interrupts any ongoing execution safely

This structure was designed to avoid visual desynchronization and to ensure that the on-screen animation matches the program logic.

---

## 13. Technical Stack

The prototype is implemented as a lightweight front-end project using:

- **HTML5**
- **Tailwind CSS** via CDN
- **Vanilla JavaScript**
- **SVG** for the stage and decorative graphics
- a local image asset: `wayang.png`

No framework or build process is required for the prototype to run.

---

## 14. File Structure

```text
Wayang-Kulit---Malaysian-Kids-Programming-Software/
├── index.html
├── wayang.png
└── README.md
```

### File descriptions

- `index.html`  
  Contains the full self-contained prototype, including layout, styling, SVG stage composition, interaction logic, and animations.

- `wayang.png`  
  Local puppet image asset used for Hanuman on the Shadow Stage.

- `README.md`  
  Project documentation prepared for coursework submission and repository reference.

---

## 15. How to Run the Prototype

### Option 1: Open directly

Open `index.html` directly in a browser.

### Option 2: Run through a local server

Recommended for more stable asset loading:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

---

## 16. Strengths of the Prototype

- strong integration of local cultural identity
- clear mapping between code actions and stage outcomes
- mobile-first interaction design
- academic annotation support for HCI reporting
- visually engaging gamified feedback
- self-contained implementation with minimal setup

---

## 17. Limitations

This project remains a high-fidelity prototype and therefore has several limitations:

- only one main level is fully implemented
- the logic vocabulary is intentionally limited
- no persistent save or progress system is included
- online CDNs are still used for styling and fonts
- educational evaluation with real child participants has not yet been conducted

---

## 18. Future Improvements

Future development could include:

- more levels and progressive difficulty
- explicit condition blocks
- multilingual support
- learner performance tracking
- teacher-facing dashboard features
- local bundling of all assets for full offline use
- empirical usability testing with the target age group

---

## 19. Course Relevance

This project is directly relevant to **Human-Computer Interaction (HCI)** because it demonstrates how usability, interaction design, visual hierarchy, feedback, and cultural context can be integrated into a working prototype.

More specifically, the project shows:

- application of HCI heuristics
- design for children’s cognitive and motor needs
- translation of abstract logic into visible interactive states
- alignment between interface behavior and learning objectives
- use of annotations to connect implementation with academic theory

For this reason, the prototype is suitable both as:

- a working front-end submission
- a demonstration artifact for presentation
- a visual reference for the written report

---

## 20. Academic Use Statement

This repository is prepared primarily for **academic coursework, prototype demonstration, and HCI evaluation**.

If the project is later published beyond the classroom, further review should be conducted for:

- asset ownership
- font licensing
- CDN dependency
- attribution requirements for third-party resources

