
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

Since its creation, at the end of 2018, there has been a strong growth in the use of technologies using 5G network, since it allows to send data at high speed.

Therefore, the exponential growth of intelligent solutions for the most varied activities, as well as the lack of technology in the market related to 5G, leads to believing that there is a good opportunity to create a solution to improve road safety, benefiting from the advantages of using this technology.

## Problem

It is necessary to develop a service whose objective is to support the traffic control entities on roads, in order to guarantee help in any situations that may occur on them.

It is intended to create a intelligent solution that takes advantage of traffic cameras and radars from the PASMO project, so that in the cloud computing environments from the 5GASP and the 5GAIner projects, it is possible to detect anomalous and relevant situations in the traffic flow of the A25, Praia da Barra and Costa-Nova.
  
If possible, we intend to implement a Car 2 Infrastructure / Infrastructure 2 Car communication using 5G, so that it is possible to exchange important information between vehicles.

## Goals

Among the most varied objectives to improve the detection of different situations on the roads, the application must provide a dashboard with information about:

### Traffic cameras and Radars from PASMO project
1. Number of vehicles to circulate (as well their velocity) at the moment and monthly
2. Traffic
3. Presence of animals, people or strange objects on the road
4. See the number of cyclists, runners or people walking on bike lanes
5. Detect inflow of the zone - with cameras estimating how many people are in Praia da Barra and Costa Nova. It also serves to tell if there are still parking spaces
6. Presence of stopped vehicles on the road

	**Nice to Have**
	1. Presence of vehicles on the side of the road
	2. The velocity on the radar can tell whether the road and the weather are in good conditions for the current velocity. If people go too fast the conditions are good

	**Future Work**
	1. Detect models of cars and check ambiental footprint taking in account max velocity allowed and model consumption

  
### Car 2 Infrastructure / Infrastructure 2 Car
1. Detect adverse conditions
	1. Rain sensors 
	2. Light sensors detect that the headlights turned on
	3. Detect if the fog headlights turned on
2. Calculate the carbon footprint by detecting the model of the car and how much it consumes
3. Warn cars if another one is coming their way with excessive speed. This can be important in terms of vehicles with priority

	**Nice to Have**

	1. Check if there are gas stations in the same road within a plausible distance, to know if with the current amount of gas/battery, a car can safely reach it. If a substantial number of cars pass with low amounts of gas and a gas station isn’t near, it might be a sign that there is a need to create a new one

	**Future Work**

	1. Explore additional features with this type of communication

  
### VNF Orchestration 

On the other end, it is important to develop a solution that is able to turn on or turn off cameras/servers programmatically, in order to manage the available resources in a better way possible. This will reduce the cost of systems renting, as a cloud service that makes available the VM´s that are used for data processing. Overall, the app may learn in which situations are necessary to change the VM´s state, e.g, if the camera goes down, the associated VM is turned off; If the camera becomes available again, the associated VM is restarted.

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

The goal of this project is to develop a set of VNF’s (Virtual Network Functions) that are capable of processing information from the video cameras and radars, notifying and storing data, using services and mechanisms made available by 5G. 

It must analyze data in order to know the number of vehicles that are driving above the speed limit, the monthly average of vehicles, etc.
Besides that, it is imperative that the system is flexible, i.e, it should be able to manage the number of cameras and radars being used, detecting when they stop streaming data.

With this system, the users will be able to use the provided data to:

- Decrease the costs of renting the VMs
- Learn when it’s in their best interest to increase/decrease the number of lanes
- Analyze statistics

With the communication between cars, it will be possible to determine the road conditions as well as to warn drivers in case of danger, such as with the arrival of vehicles at high speed.

## Related Work

## Project Calendar

Agile methodologies are applied, more specifically SCRUM, using Sprints of 2 weeks with rare exceptions.

---

### Sprint 1 - 15/03-22/03

Milestone 1 - presentation of the lifecycle objectives and calendar for the project

**Tasks**
  
1.  **Overall Project Planning**

---

### Sprint 2 - 22/03-06/04 

Milestone 2 - presentation of the lifecycle architecture; the milestone is achieved when the architecture has been validated

**Tasks** 

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

-  **(Not Planned)**

---

## Communication Plan

-  **Team Communication** - **Discord** was chosen since all team members are already familiar with the software.

-  **Backlog Management** - **Github Kanban** to record the backlog of tasks, being possible to associate each branch to an issue, track which issues are on-going, which have already been done or which are giving problems, for example. Each repository will have its issues, and there will be GitHub projects for each Sprint in the organization.

-  **Repository** - **Github** was chosen as the git platform to store the code based on an [organization](https://github.com/5g-mobility) that aggregates all the project's repositories and documentation.

-  **Git Workflow**

	The chosen workflow is based on the **feature-branching** with the following branches:

	

	-  **Master** - Main branch, where a commit is made for each release.

	

	-  **Develop** - Branch focused on development, where new branches for features come from and where they are at the end of their development.

	

	-  **Feature/*** - One branch per feature. It originates from develop and is where it is merged when finished. To merge, a pull request must be made.

	

	-  **Release/*** - This branch originates from develop and is generated at the end of each iteration, before its launch, for the final finishes. When the improvements are finished and the launch can be carried out, it is merged into the master.

	

	-  **Hotfix/*** - This branch originates from the master and is opened when there is a need to correct an error identified in production and which cannot wait for the next release to be corrected.

-  **Formal Meeting Platform** - **Zoom**

-  **File Sharing** - **Google Drive**

## Team Roles

-  **Advisor** - Prof. Diogo Gomes

-  **Co-Advisor** - Prof. Joaquim Ferreira

-  **Co-Advisor** - Prof. Rui L. Aguiar

-  **Product Owner** - Carolina Araújo

-  **Software Architect** - Hugo Almeida

-  **Team Manager** - Miguel Almeida

-  **DevOps Master** - Orlando Macedo