[![GitHub license](https://img.shields.io/github/license/microsoft/AI-For-Beginners.svg)](https://github.com/microsoft/AI-For-Beginners/blob/main/LICENSE)
[![GitHub contributors](https://img.shields.io/github/contributors/microsoft/AI-For-Beginners.svg)](https://GitHub.com/microsoft/AI-For-Beginners/graphs/contributors/)
[![GitHub issues](https://img.shields.io/github/issues/microsoft/AI-For-Beginners.svg)](https://GitHub.com/microsoft/AI-For-Beginners/issues/)
[![GitHub pull-requests](https://img.shields.io/github/issues-pr/microsoft/AI-For-Beginners.svg)](https://GitHub.com/microsoft/AI-For-Beginners/pulls/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

[![GitHub watchers](https://img.shields.io/github/watchers/microsoft/AI-For-Beginners.svg?style=social&label=Watch)](https://GitHub.com/microsoft/AI-For-Beginners/watchers/)
[![GitHub forks](https://img.shields.io/github/forks/microsoft/AI-For-Beginners.svg?style=social&label=Fork)](https://GitHub.com/microsoft/AI-For-Beginners/network/)
[![GitHub stars](https://img.shields.io/github/stars/microsoft/AI-For-Beginners.svg?style=social&label=Star)](https://GitHub.com/microsoft/AI-For-Beginners/stargazers/)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/microsoft/ai-for-beginners/HEAD)
[![Gitter](https://badges.gitter.im/Microsoft/ai-for-beginners.svg)](https://gitter.im/Microsoft/ai-for-beginners?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)


# Safety Engineering Readme

<img src="images/Safety.png" width="250">

Hey everyone! For me, committing to product safety is like an adrenaline boost. Making lives easier, safer, and better is my ultimate vision. Right now, I'm diving into Model-Based Systems Engineering (MBSE) to build a detailed system database for a machine. Maybe one day I can make a LLM AI with these data. I'll be sharing my progress and interesting links I find along the way. Join me on this exciting journey!

## Table of Contents

1. [MBSE](#1-mbse)
    - [1.1 Definition](#11-definition)
    - [1.2 Value of MBSE](#12-value-of-mbse)
    - [1.3 My thought on MBSE project](#13-my-thought-on-mbse-project)
    - [1.4 Project Mind Map](#14-project-mind-map)
2. [Legislation and Regulatory](#2-legislation-and-regulatory)
    - [2.1 Overview](#21-overview)
    - [2.2 Standard](#22-standard)
    - [2.3 Certification](#23-certification)
3. [Projects](#3-projects)
    - [2.1 Automatic Welding Tip Changing Machine](#31-automatic-welding-tip-changing-machine)
    - [2.2 Walking Cane](#32-walking-cane)
4. [Appendix](#appendix)
    - [About Mens Feng](#about-mens-feng)
    - [Contact Information](#contact-information)

## 1. MBSE

### 1.1 Definition
Model-based systems engineering (MBSE) is a formalized methodology that is used to support the requirements, design, analysis, verification, and validation associated with the development of complex systems.

[![Microsoft](https://avatars.githubusercontent.com/u/6154722?s=200&v=4?style=flat-square&logo)](https://microsoft.github.io/AI-For-Beginners/)AI-For-Beginners
[![NASA](https://avatars.githubusercontent.com/u/848102?s=200&v=4?style=flat-square&logo)](https://github.com/nasa/progpy/blob/master/README.md)NASA-Progpy 
[![NoMagic](https://avatars.githubusercontent.com/u/46573922?s=200&v=4)](https://www.3ds.com/products/catia/no-magic)Dassault Systèmes

[SysML](https://github.com/Systems-Modeling)Created by OMG supported by IBM, it has been researching in UML, SysML langudges

[PlantUML](https://plantuml.com/en/) This website shows how data can be converted into diagrams, but my question is these insturctions are not human langudge

[NoMagic](https://vimeopro.com/user28256466/no-magic-world-symposium-2016/video/171045570)NoMagic World Conference (Dassault Systèmes)


### 1.2 Value of MBSE
In today's fast-moving world, getting products to market quickly and affordably is crucial. "Traceability" – keeping track of the system's development – is essential for smooth audits and certifications, and for legal protection.

Model-Based Systems Engineering (MBSE) is a big help here. It gathers all the information in one place, saving engineers time searching through scattered documents. This not only makes compliance easier but also improves safety standards.

Plus, MBSE lets you reuse parts of the system, making development cheaper and more sustainable. By using existing models and components, you can speed up development and cut costs.


### 1.3 My thought on MBSE project

### 1.3.1 Project Objective
A database system that captures machine function data in a human-readable way, displays data relationships using graphic diagrams, and can feed into a Language Model (LM) to build a chatbot.


### 1.4 Project Mind Map

### 1.4.1 PlantML 

GPT3.5 created a sample SysML Diagram look like this below. I was quite satistfied with the result that is able to capture the hirearchy realationship of the system display in text format. I asked GPT3.5 how is this generated. It replies that this diagram is generated based of text [input](#1412-input) and [output](#1411-output) the diagram in text format. It utilized a PlanetUML liberary in python, and no use of SQL database. My summary of this system is **text ----> diagram**. This is a great start, but not quite what I am looking for...

### 1.4.1.1 Output

This is a sample SysML Block Definition Diagram, it captures the hierarchy of components and their relationships within the car system, as well as system functions related to speed and safety data. I have also using GPT3.5 to create other Model digrams which I will put them in appendix [PlantML Output Diagrams](#plantml-output-diagrams).

```plantuml
@startuml
alice->bob:hello
@enduml

PlantUML markdown integration (error)
```

```python
       +---------------------+
       |       CarSystem     |
       +---------------------+
                |
                |
      +---------------------+
      |        Car          |
      +---------------------+
      | - VIN: String       |
      | - make: String      |
      | - model: String     |
      | - year: int         |
      +---------------------+
            /        \
           /          \
  +-----------------+  +------------------+
  |     Engine      |  |   Transmission   |
  +-----------------+  +------------------+
  | - horsepower: int|  | - type: String   |
  | - displacement:  |  | - gears: int     |
  |    String         |  +------------------+
  +-----------------+
                |
                |
       +------------------+
       |     Sensor       |
       +------------------+
       | - type: String   |
       | - location:      |
       |    String        |
       +------------------+
                |
                |
       +------------------+
       |    Controller    |
       +------------------+
       | - type: String   |
       | - function:      |
       |    String        |
       +------------------+

```
<details>

<summary>Click to see Explanation</summary>

<br /><br />

- CarSystem: Represents the overall system of the car, which consists of various components

- Car: Represents the main entity in the car system, with attributes like VIN, make, model, and year

- Engine: Represents the engine component of the car, with attributes like horsepower and displacement

- Transmission: Represents the transmission component of the car, with attributes like type (e.g., automatic, manual) and gears

- Sensor: Represents various sensors in the car system, with attributes like type (e.g., speed sensor, temperature sensor) and location

- Controller: Represents electronic control units (ECUs) or controllers in the car system, with attributes like type (e.g., engine control unit, ABS controller) and function.

<br /><br />

**Relationships and System Functions:**

- The CarSystem contains a Car entity, which encapsulates the entire vehicle

- The Car has an Engine and a Transmission, which are essential components for vehicle propulsion

- The Engine provides power to the car, and the Transmission controls the distribution of this power to the wheels

- The Sensor component collects data such as speed, temperature, and pressure from various parts of the car

- The Controller component processes this data and controls various functions within the car, such as engine control and anti-lock braking system (ABS)

<br /><br />

</details>


### 1.4.1.2 Input
I asked GPT3.5 how did you produced the diagram. It told me it used the [PlantUML](https://github.com/plantuml/plantuml/blob/master/README.md) library in `python`. PlantUML allows us to define diagrams using a simple text-based syntax and then generate the corresponding diagrams.

To use PlantUML in python enviroment we need to install it from the `>terminal` using pip
```
pip install plantuml
```
<br /><br />
After that we can use it in python. ***see the sample below***
```python
from plantuml import PlantUML

# Create a PlantUML instance
uml = PlantUML()

# Define the text representations of the diagrams
requirements_diagram = """
@startuml
    package "Car Requirements" {
        package "Functional Requirements" {
            - Provide propulsion
            - Ensure safety
            - Monitor vehicle speed
        }
        package "Non-Functional Requirements" {
            - Fuel efficiency
            - Reliability
        }
    }
@enduml
"""

# Generate the diagrams
uml.processes.append(requirements_diagram)

# Render and save the diagrams
uml.render_directory('.', clean_first=True)

```
### 1.4.1.3 Feedback
To be honest, this system is not what I want for my project. But after this experience, I have a clearer vision of what I am looking for. From a top level the system should work like `Diagram --> Text.DB`. Describe the relationship between each `entity` is not very intuitive and the data is not stored in database that can be used to populate a LLM. And, with database I believe we can sync the data. Once place change will correlated to other database.

<details>

<summary>Store data in SQL Sample code</summary>

<br /><br />

```python
import sqlite3

# Connect to SQLite database
conn = sqlite3.connect('car_system.db')
cursor = conn.cursor()

# Create tables for each class
cursor.execute('''CREATE TABLE IF NOT EXISTS Car (
                    vin TEXT PRIMARY KEY,
                    make TEXT,
                    model TEXT,
                    year INTEGER
                )''')

cursor.execute('''CREATE TABLE IF NOT EXISTS Engine (
                    id INTEGER PRIMARY KEY,
                    car_vin TEXT,
                    horsepower INTEGER,
                    displacement TEXT,
                    FOREIGN KEY (car_vin) REFERENCES Car(vin)
                )''')

cursor.execute('''CREATE TABLE IF NOT EXISTS Transmission (
                    id INTEGER PRIMARY KEY,
                    car_vin TEXT,
                    type TEXT,
                    gears INTEGER,
                    FOREIGN KEY (car_vin) REFERENCES Car(vin)
                )''')

cursor.execute('''CREATE TABLE IF NOT EXISTS Sensor (
                    id INTEGER PRIMARY KEY,
                    car_vin TEXT,
                    type TEXT,
                    location TEXT,
                    FOREIGN KEY (car_vin) REFERENCES Car(vin)
                )''')

cursor.execute('''CREATE TABLE IF NOT EXISTS Controller (
                    id INTEGER PRIMARY KEY,
                    car_vin TEXT,
                    type TEXT,
                    function TEXT,
                    FOREIGN KEY (car_vin) REFERENCES Car(vin)
                )''')

# Commit changes and close connection
conn.commit()
conn.close()

```

<br /><br />

</details>

### 1.4.2 Opensource/Free MBSE Application

SysML Modeling Tools (e.g., Cameo Systems Modeler Community Edition, Papyrus):

[Cameo Systems Modeler Community Edition](https://www.3ds.com/products/catia/no-magic/cameo-systems-modeler) Cameo Systems Modeler offers a free Community Edition with limited features but includes basic support for database storage and integration.

[Papyrus](https://eclipse.dev/papyrus/relatives.html) 🍍 Papyrus is an open-source modeling tool that supports SysML and UML. It offers database integration features and is available for free as part of the Eclipse Modeling Tools distribution.
OpenMBEE (Open Model-Based Engineering Environment):

[OpenMBEE](https://github.com/Open-MBEE) 💓 is an open-source platform for model-based engineering that provides tools and resources for collaborative modeling. It offers database storage capabilities and is freely available for use.
Modelio Community Edition:

Modelio is an open-source modeling tool that supports various modeling standards, including SysML and UML. The Community Edition is free to use and includes basic database integration features.
Capella:

Capella is an open-source MBSE tool specifically designed for systems architecture modeling. It supports database storage and integration and is freely available for download.
OpenModelica:

OpenModelica is an open-source modeling and simulation environment for cyber-physical systems. While primarily focused on simulation, it includes capabilities for database storage and management of models.
Simulink:

Simulink, while not open-source, offers a free trial version and a limited-feature version called Simulink Coder. Simulink supports modeling and simulation of cyber-physical systems and includes database integration features.

### 1.4.3 Operation Solution

After getting to know PlantUML little better, I think the reason why it is popular is because it changed the way how these diagrams used to be developed. Started with `diagram` then convert it into `code` even `database` with entity relationships. Diagrams are created by coding the relationship between each entitiies. This method is not intuitive as first sight, but it can potencially reduce the number of re-edit the diagram manually. It sure limmits the freedom of manipulating the diagram layout, but it offers a more robust and efficient way to produce diagrams. Moreover, it enphasis the entity relationship as the developer creates the diagram. I have to start using it to find out if this is the solution for this problem.

<br /><br />
## 2. Legislation and Regulatory

### 2.1 Overview
The area of medical device engineering is heavily regulated. Practicing systems design engineers must consult and cooperate with regulatory law, attorneys, and other experts. The resources in this guide can help you find legislative and regulatory information from Canada and the United States.

### 2.1.1 Commercial Product vs Industrial Solution
A commercial product is intended for purchase on the market by customers. Before launch, it must undergo a thorough process that includes patent protection, public disclosure, and licensing agreements to ensure viability and compliance with guidelines.
On the other hand, an industrial solution may be developed in-house to support manufacturing processes. For example, a company may design a robot arm for use on a production line to automate tasks. In this scenario, the company faces two options: 
1. **Commercialization**: The company can choose to commercialize the robot arm, selling it to other companies to generate profit. To do so, it must obtain necessary certifications to comply with federal regulations, such as the [Canada Consumer Product Safety Act](https://laws-lois.justice.gc.ca/eng/acts/c-1.68/FullText.html), in the specified region.
2. **In-house Use**: Alternatively, the company may opt to use the robot arm solely within its own facilities to optimize production processes as an improvement solution. In this case, the company must carefully consider safety risks associated with using the arm in-house to prevent harm or danger to human health. Additionally, it must adhere to regulations governing the operation of the robot arm within its facility.


### 2.2 Standard

### 2.3 Certification

### 2.4 Accreditation




<br /><br />
## 3. Projects

### 3.1 Automatic Welding Tip Changing Machine



- Leading the development of an automated system that can replace the weld tip on a welding robot, reducing both production cycle time and the need for human intervention

- Adapting industrial communication protocols to better suit the factory environment and ensure safe communication with existing machines through a handshake mechanism

### 3.2 Walking Cane



Successfully designing and crafting a walking cane for the average Canadian, integrating CNC milling and turning operations, and validated the structural integrity through Finite Element Analysis (FEA)



<br /><br />
## Appendix

### PlantML Output Diagrams

1. SysML Requirements Diagram:

```python
    +-------------------------+
    |       Car Requirements   |
    +-------------------------+
              |
              |
    +-------------------------+
    |      Functional         |
    |    Requirements         |
    +-------------------------+
    | - Provide propulsion    |
    | - Ensure safety         |
    | - Monitor vehicle speed |
    +-------------------------+
              |
              |
    +-------------------------+
    |    Non-Functional       |
    |    Requirements         |
    +-------------------------+
    | - Fuel efficiency       |
    | - Reliability           |
    +-------------------------+

```

2. SysML Activity Diagram:

```python
          +---------------------------+
          |     Start Engine           |
          +---------------------------+
          |                           |
+------------------------+    +-----------------------------+
|   Check Fuel Level     |    |    Ignition Key Turned      |
+------------------------+    +-----------------------------+
|   If fuel is low,      |    |  If ignition key is turned, |
|   display warning      |    |  send signal to start engine|
+------------------------+    +-----------------------------+
|   Otherwise, proceed   |    |        Start Engine         |
|   with ignition        |    +-----------------------------+
+------------------------+

```

3. SysML State Machine Diagram:

```python
      +-----------------------------+
      |         Engine State         |
      +-----------------------------+
          |                    |
    +-----------+          +------------+
    |  Off      |          |   Running  |
    +-----------+          +------------+
      |    |                   |     |
      |    | Ignition key     |     | Engine running
      |    +------------------+     |
      |          Engine off         |
      +-----------------------------+

```

4. SysML Sequence Diagram:

```python
   +-------------------------------+
   |     User - Car Interaction    |
   +-------------------------------+
            |                |
            | Start Engine   |
            |--------------->|
            |                |
            |                |
            | Engine Started |
            |<---------------|
            |                |
            |                |
            | Check Speed    |
            |--------------->|
            |                |
            | Speed Data     |
            |<---------------|
            |                |
            | Stop Engine    |
            |--------------->|
            |                |
   +-------------------------------+

```

### Estimated DevOP Timeline and Staff by GPT3.5

| Team Member         | Responsibilities                                                                                                       | Expertise                                                                                                            | Number of People |
|---------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------|
| Database Developer  | Designing the database schema, creating tables, defining relationships, and optimizing database performance.          | Database management systems (e.g., SQLite, MySQL, PostgreSQL), SQL query optimization                                | 1                |
| Backend Developer   | Implementing CRUD operations for data management, integrating with the database, implementing business logic, and API endpoints. | Backend programming languages (e.g., Python, Java, Node.js), web frameworks (e.g., Flask, Django, Express.js) | 1                |
| Frontend Developer  | Developing user interfaces for displaying diagrams and interacting with the system.                                    | Frontend technologies (e.g., HTML, CSS, JavaScript), web frameworks (e.g., React, Angular, Vue.js)                  | 1                |
| Full Stack Developer (optional) | Combining backend and frontend development, implementing end-to-end functionality, and coordinating between different components. | Both backend and frontend technologies.                                                                             | 1 (Optional) |


---

### Timeline:

#### Database Design and Setup (2 weeks):
- Designing the database schema based on requirements.
- Setting up the database and creating tables.

#### Backend Development (4 weeks):
- Implementing CRUD operations for data management.
- Developing APIs for retrieving and storing data.
- Integrating with the database.

#### Frontend Development (4 weeks):
- Designing user interfaces for displaying diagrams.
- Implementing functionality for interacting with diagrams and data.

#### Integration and Testing (2 weeks):
- Integrating backend and frontend components.
- Testing the system for functionality, performance, and reliability.

#### Deployment and Launch (1 week):
- Deploying the system to a production environment.
- Conducting final checks and ensuring readiness for launch.

**Total Time:** 13 weeks (approximately 3 months)

---

### About Mens Feng

Mens Feng is a seasoned safety engineer with a passion for leveraging technology to improve safety standards. With a background in mechanical engineering and a knack for innovation, Mens Feng has spearheaded numerous projects that have garnered recognition for their impact on safety and efficiency.

### Contact Information

&nbsp;<div align="center">
  [Fork](https://github.com/novatorem/novatorem/blob/main/SetUp.md) this [unlicensed](https://choosealicense.com/licenses/unlicense/) repository to recreate!<br><br>
  [![Linkedin](https://img.shields.io/badge/linked-in-369?style=flat-square&logo=linkedin&logoColor=white&color=blue)](https://www.linkedin.com/in/mens-feng-53356016b/)
  [![E-Mail](https://img.shields.io/badge/email-reveal-2a8?style=flat-square&logo=gmail&logoColor=white)](https://mail.novac.dev/)
  [![Visits](https://komarev.com/ghpvc/?username=novatorem&logo=GitHub&label=github%20visits&color=336699&logoColor=white&style=flat-square)](https://github.com/novatorem)
</div>
