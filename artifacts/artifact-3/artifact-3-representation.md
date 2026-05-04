# Artifact 3 - Representation

---

## System Capability

### Which capability we are implementing

We continued working on the *Recipe Based Deficit Calculation* capability that was selected and designed in artifact 2.  

This capability lets the Quartermaster (Sam) or each individual user select a recipe and automatically compares the required ingredients with the Fellowship's shared inventory.  
The system then shows what is missing and in what quantity, so the group can decide whether to cook the meal, adjust the parameters (people, days, buffer day), pick a different recipe or plan a resupply.

In Assignment 2 we designed how the capability works by utilizing the Mermaid flowchart and what the uid looks like by using wireframe. In this assignment we translate the wireframe into a HTML and CSS page.


### Why this capability matters for the Fellowship at this stage of the journey

The Fellowship is currently moving through harsh wilderness with limited resupply opportunities. Food is now a survival resource that must be planned, not improvised.  

Without an automated check, the Quartermaster would have to manually estimate quantities and remember everything correctly under pressure. This is slow and prone to be full of errors, two things the group cannot afford in their current situation.  

The capability matters at this exact stage because:  
- Resupply is rare and unreliable.  
- Mistakes at markets are expensive.  
- Silence keeps the group safe.  
- Decisions must be fast.

This capability turns a chaotic, manual check into a quiet, reliable decision. That is exactly what the Fellowship needs while pressing further into hostile country.

---

## Static Interface Implementation

[Artifact 3 - Interface](https://the-fellowship-of-the-five.github.io/The-Fellowship-of-the-Code-2026/artifacts/artifact-3/src/interface.html)

### HTML Page

[Interface.html](https://github.com/The-Fellowship-of-the-Five/The-Fellowship-of-the-Code-2026/blob/main/artifacts/artifact-3/src/interface.html)

### CSS Page

[style.css](https://github.com/The-Fellowship-of-the-Five/The-Fellowship-of-the-Code-2026/blob/main/artifacts/artifact-3/src/style.css)

---

## Design Rationale

### How does this interface support the intent and value defined in Assignment 1?
In Assignment 1, we established that the system must relieve the group (mostly Sam) from chaotic, manual inventory checks and support quiet, fast decision-making in good and bad situations. The created interface supports that by providing a clear, step-by-step flow which includes three sites: Mode, Parameters and Recipe source. By using semantically correct fields with strict min constraints, we prevent the entry of invalid data, for example negative travel days, which is critical for ensuring the system calculates a reliable, error- and stress-free output later.

### How does it reflect the wireframe from Assignment 2?
The implementation translates the structure of wireframes into a concrete layout. For this we took the first four screens(from planning mode to recipe selection) and put the raw structures from the picture into semantic HTML forms. Sam most likely only has space for a phone, therefore a desktop version will not be needed. Because of that we used a constrained phone-shell layout and ensured consistent alignment and spacing across all elements.

### What did you deliberately not implement yet?
As instructed, the page relies purely on HTML and CSS. There is no JavaScript or backend logic.

- While there are simulated inputs like changing the number of people, there are no actual calculations involved.
- The Button "Show recipes that fit" is a static link to the next screen with no measured and calculated data involved.
- We focused this implementation on the setup and parameter flow of the capability and left out the final screens to prioritize structure over completeness.

### What assumptions or constraints shaped your decisions?

- Constraints: We were restricted to HTML & CSS and could not use JavaScript or Frameworks. This forced us to rely on CSS flexbox for stability and tricks to make a multi-screen flow.
- Assumptions: We assumed that the Fellowship will only use this app on mobile devices. Because of this, we optimized the UX for touch: We hid default browser arrows on number inputs, removed the "Continue" buttons and added a "Back" button to all sites.








