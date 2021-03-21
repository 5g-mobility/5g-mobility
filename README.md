
  
# 5G Mobility Documentation

  

### Table of contents

  

*  [Inception Phase](#inception-phase)

*  [Context](#context)

*  [Problem](#problem)

*  [Goals](#goals)

*  [Tasks](#tasks)

*  [Expected Results](#expected-results)

*  [Related Work](#related-work)

*  [Project Calendar](#project-calendar)

*  [Communication Plan](#communication-plan)

*  [Team Roles](#team-roles)

  
  

# Inception Phase

  

## Context

In 2019, 35.704 accidents with victims on Portuguese roads were reported, of which 626 resulted in fatal victims, 2.168 seriously injured and 43.183 with light injuries.

Since its creation, at the end of 2018, have noticed a strong growth in the use of technology using 5G network, since it allows send of data at high speed.

Therefore, the exponential growth of intelligent solutions for the most varied activities, as well as the lack of technology in the market related to 5G ( introduced only at the end of 2018), leads to wanting that there is a good opportunity to create a solution to improve road safety, benefiting from the advantages of using this technology.
  

## Problem

  It is necessary to develop a service whose objective is to support the traffic control entities on highways, in order to guarantee help to any situations that may happen on them.

It is intended to create a intelligent solution that takes advantage of traffic cameras and radars from PASMO project, so that in the cloud computing environments from 5GASP and 5GAIner projects, it is possible to detect anomalous and relevant situations in the traffic flow of the A25, Praia da Barra and Costa-Nova.

If possible, intends also to implement a v2v communication using 5G, so that it is possible to exchange important info between vehicles.

## Goals

  

## Tasks

  

**Car Communication (Hugo Almeida e Orlando Macedo)**

  

1. Research OBDII protocol

2. Implement a car emulator to receive and generate data

  

**VNF Orchestration (Hugo Almeida e Miguel Almeida)**

  

1. Research about VNF in 5G

2. Integrate developed VNF into 5GASP testbed

  

**Computer Vision (Miguel Almeida, Orlando Macedo e Carolina Araújo)**

  

1. Research for Machine Learning and pattern recognition tools

2. Train a custom Object Detection Model

  

**Backend (Carolina Araújo e Hugo Almeida )**

  

1. Define what database to use for each scenario

2. Create the databases schema

3. Define the endpoints necessary to the API

  
  

**Frontend (Carolina Araújo e Hugo Almeida)**

  

1. Design and develop an interface for the web applications

  

**CI Pipeline (Orlando Macedo e Miguel Almeida)**

  

1. CI Pipeline

  
  

## Expected Results

  

## Related Work

  

## Project Calendar

  

Agile methodologies are applied, more specifically SCRUM, using Sprints of 2 weeks with rare exceptions.



### Sprint 1 - 15/03-22/03

  

Milestone 1 - presentation of the lifecycle objectives and calendar for the project

  

### Tasks

  

1.  **Overall Project Planning**

  

---

### Sprint 2 - 22/03-06/04

  

Milestone 2 - presentation of the lifecycle architecture; the milestone is achieved when the architecture has been validated

  

### Tasks

  

1.  **Car Communication #1**

2.  **Computer Vision #1**

3.  **Backend #1**

  

---

### Sprint 3 - 06/04-21/04

  

Milestone 3 - prototype; mid-term presentation with supervisors; peer evaluation

  

**Tasks**

  

1.  **Car Communication #2**

2.  **Computer Vision #2**

3.  **Backend #2**

4.  **CI Pipeline #1**

5.  **Frontend #1**

  

---

### Sprint 4 - 21/04-06/05

  

Milestone 3 - prototype; mid-term presentation with supervisors; peer evaluation

  

**Tasks**

  

1.  **Car Communication #3**

2.  **Computer Vision #3**

3.  **Backend #3**

4.  **CI Pipeline #2**

5.  **Frontend #2**

6.  **VNF Orchestration #1**

  

---

### Sprint 5 - 06/05-17/05

  

Milestone 3 - prototype; mid-term presentation with supervisors; peer evaluation

  

**Tasks**

  

1.  **Car Communication #4**

2.  **Computer Vision #4**

3.  **Backend #4**

4.  **CI Pipeline #3**

5.  **Frontend #3**

6.  **VNF Orchestration #2**

  

---

### Sprint 6 - 17/05-01/06

  

Milestone 4 - project presentation; all functionality has been developed

  

**Tasks**

  

1.  **Technical report #1**

2.  **Polish overall project #1**

  

---

### Sprint 7 - 01/06-16/06

  

Milestone 4 - project presentation; all functionality has been developed

  

**Tasks**

  

1.  **Technical report #2**

2.  **Polish overall project #2**

  

---

### Sprint 8 - 16/06-21/06

  

Milestone 4 project presentation; all functionality has been developed

  

**Tasks**

  

(Not Planned)

  
  

## Communication Plan

- **Team Communication** - **Discord** was chosen since all team members are already familiar with the software.

- **Backlog Management** - ** Github Kanban ** to record the backlog of tasks, being possible to associate each branch to an issue, track which issues are on-going, which have already been done or which are giving problems, for example. Each repository will have its issues, and there will be GitHub projects for each Sprint in the organization.

 - **Repository** - Github was chosen as the git platform to store the code based on an [organization] (https://github.com/5g-mobility) that aggregates all the project's repositories and documentation.

- **Git Workflow** 

	The chosen workflow is based on the ** feature-branching ** with the following branches:

	- **Master** - Main branch, where a commit is made for each release.

	- **Develop** - Branch focused on development, where new branches for features come from and where they are at the end of their development.

	- **Feature/*** - One branch per feature. It originates from develop and is where it is merged when finished. To merge, a pull request must be made.

	- **Release/*** - This branch originates from develop and is generated at the end of each iteration, before its launch, for the final finishes. When the improvements are finished and the launch can be carried out, it is merged into the master.

	- **Hotfix/*** - This branch originates from the master and is opened when there is a need to correct an error identified in production and which cannot wait for the next release to be corrected.

- **Formal Meeting Platform** - Zoom

- **File Sharing** - Google Drive

  

## Team Roles

- **Advisor** - Prof. Diogo Gomes

- **Co-Advisor** - Prof. Joaquim Ferreira

- **Co-Advisor** - Prof. Rui L. Aguiar

- **Product Owner** - Carolina Araújo

- **Software Architect** - Hugo Almeida

- **Team Manager** - Miguel Almeida

- **DevOps Master** - Orlando Macedo