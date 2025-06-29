## Domain Glossary System Context Diagram

## How to View the ER Diagram

The Mermaid `erDiagram` syntax may not render properly on this site due to limitations of the current Mermaid version.

To view the ER diagram correctly, follow these steps:

---

## 📤 Steps to View in Mermaid Live Editor

1. Open the [Mermaid Live Editor](https://mermaid.live/edit).
2. Copy the content below and paste it into the left-hand editor panel.
3. Click the **"Full screen"** button in the top-right to expand the diagram.

---

## 📋 Diagram Code (copy this)

```mermaid
C4Context
    title Context diagram for Domain Glossary System
    Boundary(dgsBoundary, "Domain Glossay System Boundary") {
        Person(admin, "Admin", "A user who is going to resposnible <br/> to manage organizations, <br/> users and other everything")        
        Person(managers, "Managers", "A user who is going to resposnible <br/> to manage projects, <br/> contexts,terms and project assignment")        
        Person(members, "Members", "A user who is belongs to <br/> one or many projects <br/> and know project doamin using context and terms")

        System(doaminGlossarySystem, "Domain Glossary System", "Allows managers to manager <br/> glossary of doamin")        
        
    }

    Rel(admin, doaminGlossarySystem, "Uses")
    Rel(managers, doaminGlossarySystem, "Uses")
    Rel(members, doaminGlossarySystem, "Uses")

UpdateLayoutConfig($c4ShapeInRow="2", $c4BoundaryInRow="1")

```
