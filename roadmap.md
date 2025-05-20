# Technical Roadmap: Local AI Storyteller RPG (Gemini SDK Edition with GUI)

**Project Goal:** To develop a locally runnable, **graphically engaging GUI-based AI Role-Playing Game (RPG)** similar to AI Dungeon. The core text generation will be powered by Google's Gemini models. A key feature will be achieving a **beautiful, immersive RPG-style user interface** and playing scenarios based on a user-specified {series}.

**Version:** 1.2
**Date:** 2025-05-20

**Core Assumption:** The application will have a dedicated, **stylized GUI** and run locally. Core AI generation relies on the Gemini API. The game will focus on interactive RPG storytelling with a high-quality visual presentation.

---

## Phase 0: Foundation, Research & Visual Design (3-4 Weeks)

**Objective:** Establish the development environment, select core technologies including a **GUI framework optimized for custom styling**, define the **visual style and RPG aesthetics** for the UI, and understand Gemini model capabilities.

* **1. Technology Stack Definition:**
    * **Programming Language:** Python (for unified backend/frontend development and strong AI SDK support).
    * **LLM Interaction Library:** `google-generativeai`.
    * **User Interface (UI) Framework Selection (Emphasis on Aesthetics & Customization):**
        * **Top Contenders for an RPG UI:**
            * **PyQt6/PySide6:** Highly customizable via QSS (CSS-like stylesheets) and custom widgets. Excellent for a polished, professional RPG feel.
            * **Kivy:** Ideal for unique, non-native looking UIs with custom graphics and animations. Uses Kv language for design.
            * **CustomTkinter:** For a modern, themed Tkinter experience if a simpler approach is desired but still visually appealing.
            * **Dear PyGui:** Consider for performance and immediate mode GUI if it fits the desired style.
        * **Decision Criteria:** Developer familiarity, desired level of visual customization, specific RPG style requirements, performance needs.
    * **Data Storage:** JSON, YAML, or SQLite.
    * **Vector Database (for RAG):** FAISS, ChromaDB, LanceDB.
* **2. Visual Style Guide & UI/UX Design for RPG Theme:**
    * **Research & Mood Boarding:** Gather inspiration for RPG UIs (fantasy, sci-fi, etc., based on target {series} types).
    * **Define Core Aesthetics:**
        * **Color Palette:** Primary, secondary, accent colors fitting the RPG mood.
        * **Typography:** Select thematic fonts for headings, body text, UI elements.
        * **Iconography:** Style for icons (inventory, actions, etc.).
        * **Widget Design:** Concepts for custom-looking buttons, scrollbars, frames, text areas.
        * **Layout Principles:** Plan the arrangement of story display, input, character sheet, inventory, map (if any).
    * **Create Basic UI Mockups/Sketches:** Visualize key screens reflecting the RPG style.
* **3. Gemini Model Selection & API Setup:**
    * As per previous roadmap (research models, API key, SDK setup, basic RPG prompt tests).
* **4. Initial RPG Mechanics Definition:**
    * As per previous roadmap (player character, inventory, basic states).
* **5. Development Environment Setup:**
    * As per previous roadmap.
* **6. Initial {Series} Research (RPG & Visual Focus):**
    * Gather lore, but also visual cues, art styles, and typical UI elements from the chosen {series} to inform your UI design.

---

## Phase 1: Core RPG Engine & Foundational RPG-Styled GUI (5-8 Weeks)

**Objective:** Implement the fundamental RPG loop with Gemini and a functional GUI that **from the outset incorporates elements of the defined RPG visual style.**

* **1. Gemini SDK Integration Module:** As per previous roadmap.
* **2. Basic RPG Game Loop & State Management:** As per previous roadmap.
* **3. Prompt Engineering - Iteration 1 (RPG GM Persona):** As per previous roadmap.
* **4. Foundational GUI Implementation (RPG Styled):**
    * Using the chosen GUI framework:
        * Implement the main application window with the defined RPG theme (backgrounds, basic window dressing).
        * Create a scrollable text area for story/narration, styled according to the visual guide (font, colors).
        * Implement the player input field and "Send" button with custom RPG styling.
        * Develop initial display areas for character name and inventory, applying thematic styling.
        * **Focus:** Ensure even these basic elements reflect the target RPG aesthetic, avoiding purely default widget appearances. This might involve creating simple custom widgets or applying initial stylesheets.

---

## Phase 2: {Series}-Specific RPG Scenarios & Iterative GUI Styling (5-8 Weeks)

**Objective:** Enable loading of {series}-specific RPG scenarios and **iteratively refine and expand the GUI's RPG styling and custom components.**

* **1. Scenario Definition Structure (RPG Focus):** As per previous roadmap.
* **2. Scenario Loader & Initializer (with GUI Integration):**
    * GUI elements (e.g., styled list or card view) to browse and select scenarios.
* **3. Prompt Engineering for {Series} RPG Adaptation:** As per previous roadmap.
* **4. GUI Styling & Custom Widget Development - Iteration 1:**
    * **Apply Theming:** Systematically apply the defined color palette, fonts, and basic styles across all existing UI elements.
    * **Develop/Customize Key Widgets:**
        * Enhance the inventory display with more RPG-appropriate visuals (e.g., item slots, styled lists).
        * Begin work on a dedicated character status panel using RPG-themed elements.
    * **Refine Layout:** Ensure ergonomic flow and visual hierarchy.
    * Implement Save/Load game functionality with styled dialogs/UI elements.

---

## Phase 3: Advanced RPG Features & Deep GUI Customization/Polish (Ongoing)

**Objective:** Add depth to RPG mechanics and **achieve a highly polished, beautiful, and immersive RPG user interface through extensive customization and thematic asset integration.**

* **1. Save/Load Game Functionality (Polished GUI):** As per previous roadmap.
* **2. Enhanced RPG State Management & Mechanics:** As per previous roadmap.
* **3. Deep GUI Customization & RPG Immersion:**
    * **Advanced Custom Widgets:** Implement highly stylized widgets (e.g., ornate scrollbars, custom-bordered frames, animated buttons if desired and framework supports easily).
    * **Thematic Asset Integration:** Incorporate graphical assets:
        * Custom backgrounds for different panels or game states.
        * Thematic borders and dividers.
        * Custom icons for items, actions, character conditions.
    * **Dedicated RPG Panels (Fully Styled):**
        * **Inventory Management:** Visually rich display, possibly with drag-and-drop, item icons, tooltips.
        * **Character Sheet:** Aesthetically pleasing display of stats, equipment, conditions, portrait.
        * **Quest Log/Journal:** Styled to look like an in-game journal.
        * **Map Area (Optional):** If implemented, style it thematically (e.g., old parchment, holographic display).
    * **UI Animations & Transitions (Subtle):** If supported by the framework (e.g., Kivy, PyQt with QML/Animations), add subtle effects to enhance UX without being distracting.
    * **Accessibility Considerations:** Ensure good contrast, readable fonts, and keyboard navigation.
* **4. Context Window Management:** As per previous roadmap.
* **5. Multimodal RPG Elements (Optional):** As per previous roadmap.

---

## Phase 4: Advanced {Series} Customization & RAG for RPGs (Optional, Advanced)

**(Largely unchanged, but RAG outputs will populate the beautifully styled UI)**
* **1. Full Retrieval Augmented Generation (RAG) for RPG Lore:** As per previous roadmap.
* **2. Fine-Tuning Gemini for Specific RPG Styles/Series:** As per previous roadmap.
* **3. User-Defined RPG Scenarios & {Series} Configuration (via Styled GUI):**
    * If allowing users to create scenarios, the interface for this should also be themed and user-friendly.

---

## Phase 5: Testing, Packaging & Documentation (Ongoing)

**Objective:** Ensure a high-quality, visually stunning, and playable RPG experience.

* **1. Testing:**
    * **UI/UX Testing:** Rigorous testing of all visual elements, themes, custom widgets, responsiveness across different states, and overall aesthetic appeal.
    * **RPG Mechanics & Gameplay Testing.**
* **2. Performance & API Usage Monitoring:** As per previous roadmap.
* **3. Documentation:**
    * User Manual: Including guidance on navigating the RPG-styled GUI.
* **4. Packaging & Distribution:** As per previous roadmap.

---

## Key Considerations for GUI-Based AI Storyteller RPG (Emphasis on Visuals):

* **Early Focus on Visual Design:** Don't leave UI styling as an afterthought. Integrate it from Phase 0/1.
* **Choosing the Right GUI Framework:** Critical for achieving the desired level of customization.
* **Iterative Design & Prototyping:** Continuously refine the UI based on playtesting and visual goals.
* **Balance Aesthetics with Usability:** A beautiful UI must also be intuitive and easy to use.
* **Asset Creation/Sourcing:** Plan for how you will create or source thematic graphical assets (icons, borders, textures).

---
