---
title: "Design"
teaching: 0
exercises: 0
questions:
- "Creating a component Diagram"
- "..."
objectives:
- ""
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

# Component Diagrams
A component diagram is a useful high level design diagram showing high level components and their dependencies.
This type of diagram is very useful to describe how code is organized into components and how to break up large
projects into smaller components. This type of diagram is useful to communicate with team members this composition
and to have a shared understanding of the dependencies between components. 

Without such a diagram code will normally evolve into a speggetti code of dependencies.

# Start With Existing System
Often in a project we are starting from an existing system. It is always a good idea to create a diagram of the existing system first.
Finly knows little about the Dam project of Ben the Beaver so his initial component diagram might look like this.

<img src="../figures/ComponentDiagram1-LegacyComponent.drawio.png" alt="Initial Existing System" style="height: 250px"/>

This is very simple, but at least shows the external inputs and outputs of the system. This is a better overview than
just looking at directories of source code.

# Adding More Detail
The next thing that Finly tries is to look at the existing source code and try create sub-components to represent collections of code.
He is still just trying to describe the existing system so his next version of a component diagram might look like this.

<img src="../figures/ComponentDiagram1-FirstComponents.drawio.png" alt="Raw Detail" style="height: 250px"/>

At this point our component diagram is showing a lot of information. 
The subcomponent boxes represent either files or packages (directories of files) of the source code.
The arrows show when code in one box calls or makes reference to code in another box.

It appears that the code is a giant mess of spegetti code.
Left to evolve you can imagine that new developers will add new code and new dependencies. Without any rules to know what 
is allowed to call what this will get more and more complex and harder to understand. However, this diagram makes visible
at high level some organization in the existing code. This diagram can be used in discussions with the team how to improve the
code or how to understand the existing code.

# Create Higher Level Abstraction

The previous diagram is a mess, but after Finley talks to Ben the Beaver he learns that the components can understood to be clustered
into groups of components with a specific purpose. With the help of Ben they together create this component diagram.
<img src="../figures/ComponentDiagram1-Component-Interfaces.drawio.png" alt="Raw Detail" style="height: 250px"/>


{% include links.md %}

