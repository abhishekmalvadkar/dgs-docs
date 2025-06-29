## Domain Glossary System Container Diagram

## How to View the ER Diagram

The Mermaid `erDiagram` syntax may not render properly on this site due to limitations of the current Mermaid version.

To view the ER diagram correctly, follow these steps:

---

## 📤 Steps to View in Mermaid Live Editor

1. Open the <a href="https://mermaid.live/edit" target="_blank" rel="noopener">Mermaid Live Editor</a>.
2. Copy the content below and paste it into the left-hand editor panel.
3. Click the **"Full screen"** button in the top-right to expand the diagram.

---

## 📋 Diagram Code (copy this)

```mermaid
    C4Container
    title Container diagram for Domain Glossary System

    System_Ext(google_auth_server, "Google Auth Server", "Responsible to authenticate users <br/> using sign with google")
    Person(admin, "Admin", "A user who is going to resposnible <br/> to manage organizations, <br/> users and other everything")
    Person(managers, "Managers", "A user who is going to resposnible <br/> to manage projects, <br/> contexts,terms and project assignment")        
    Person(members, "Members", "A user who is belongs to <br/> one or many projects <br/> and know project doamin using context and terms")
    System_Ext(fcs_blob_storage, "Firebase Clound Storage", "Responsible to store binary files <br/> like images, pdf, videos, audios etc..")


    Container_Boundary(c1, "Domain Glossary System") {
        Container(spa, "Single Page App", "Angular", "Provides all the domain glossary management <br/> functionality to users via <br/>their web browser")
        Container(dgs_backend_system, "Backend", "Java, Spring Boot", "Microservice aarchitecture based backend")
        ContainerDb(dgs_db, "Database", "MySQL Database", "Stores dgs related data to database")
    }

    Rel(admin, spa, "Uses", "HTTPS")
    Rel(managers, spa, "Uses", "HTTPS")
    Rel(members, spa, "Uses", "HTTPS")

    Rel(spa, google_auth_server, "Uses")
    Rel(spa, fcs_blob_storage, "Uses")

    Rel(dgs_backend_system, google_auth_server, "Uses")
    Rel(dgs_backend_system, fcs_blob_storage, "Uses")

    BiRel(spa, dgs_backend_system, "Uses")
    BiRel(dgs_backend_system, dgs_db, "Uses")
    

    UpdateLayoutConfig($c4ShapeInRow="3", $c4BoundaryInRow="1")
    

```
