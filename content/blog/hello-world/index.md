---
title: "Deliverable 1: Observations and Proposal"
date: "2015-05-01T22:12:03.284Z"
description: "Obersvations of users, Personas, Problems identified, Use Case Scenario, Finding related products, Comparing the Products, Designing at a High level, Justifying feasibility"
---
# Table of Contents
1. [Overview ✏️](#overview)
2. [Observing Users 👥](#users)
3. [The Problem 📛](#problem)
4. [Personas 👱‍♂️](#personas)
5. [Use Case Scenario](#usecase)
6. [Related Products](#products)
7. [Comparing The Products](#comparing)
8. [Designing at a High Level](#high)
9. [Justifying Feasibility](#just)

# Overview ✏️ <a name="overview"></a>
The world is waking up to the fact that climate change is a grave threat. Industry, academia and society is realizing that we need to assess the environmental impact of everything that we do. A big part of this is doing a complete assessment of the environmental impact associated with all of the stages of the life cycle of a product. In the field, this is known as life-cycle assessment.

Researchers and engineers need to use a LCA software. The most popular free open source option available right now is openLCA. While it is a powerful platform, it can be very unintuitive to use. Mostly because it looks like this.

# Observing Users 👥 <a name="users"></a>
For the initial stage we observed 3 users completing the same case study. The case study was vocally led by a facilitator. The facilitator followed the tutorial in a sequential manner, leaving the very little description of the required actions. The participants obtained additional support either from selected parts of the tutorial or selected videos only once the facilitators had decided the participant would not be able to pursue the step.

## Participants <a name="participants"></a>
### Beginner (Subject 1)
- Is currently a STEM student and has used openLCA for some analysis group projects.
- Is currently a STEM student and has used openLCA for some analysis group projects.


### Expert (Subject 2)
* More advanced PHD student who uses openLCA regularly
* Followed trainings by GreenDelta
* Has taught OpenLCA tutorials, witnessing many mistakes

### Novice (Subject 3)
* No Experience with openLCI
* Potential future user: a graduate student in Sustainability and GIS
* Strong background with open source GIS tools

#### Documents/Material for each User Observation:
TODO

# The Problem 📛
The main problem of the world's most popular free LCA software is how unintuitive it is. There are many UI related issues and is prone to many pitfalls, even by experts, which result in the inaccuraccy of the LC Analysis. 

A typical LCA has these main steps:
* Importing a Database
* Creating and configuring Flows
* Creating and configuring Processes
* Creating and configuring Product Systems
* Setting up a Project and Obtaining the final analysis report

All of these stages has multiple UI issues, which were collected during our user observations. In the documents attached, you will see a collection of these interaction problems, and a summarised solution for each of them.

### TODO: Document listing all the issues
#### Other documents/screenshots/files

# Personas 👱‍♂️ <a name="persona"></a>

### TODOS: Task based segmentation
### Subject 1 - Joe
![alt text](./persona-1.png)

### Subject 2 - Bilal
![alt text](./persona-2.png)

# Use Case Scenario 💡

### Scenario Illustration

# Related Products
# Comparing the Products
# Designing at a High Level

### Design of current openLCA tech stack
OpenLCA is a JAVA-based open-source application that is built on the Eclipse Rich Client Platform. The RCP platform provides the necessary tool kits and widgets for it to be a functional desktop-based application. The openLCA application consists of 4 key sub-projects.
olca-app: contains the source code of the openLCA RCP application.
olca-app-build: contains the build scripts for compiling openLCA and creating the installers for Windows, Linux, and macOS.
olca-app-html: contains the source code for the HTML views in openLCA (like the start page or the report views).
olca-refdata: contains the current reference data (units, quantities, and flows) that are packaged with openLCA.
The application depends on the olca-modules, which provide the main functionalities and the core APIs, as a maven project.
LCA Collaboration Server contains the remote data repositories for the application to use.
![alt text](./old-design.png)

### Design of Proposed Solution
Our proposed system will potentially create a new thin UI layer over the existing openLCA application, in hopes of improving the interaction and UX. Technologies such as NodeJS, HTML, CSS and JS will be required to build the front-end UI. A popular framework ReactJS can be used to create the UIs and interactive buttons, and using ElectronJS and NodeJS, it will communicate with the existing eclipse RCP application. The integration to the core openlca-modules and database manipulation will allow for the changes to be reflected back to the front-end

![alt text](./new-design.png)

# Justifying Feasibility