# Architectural Kata: Summer 2022: Spotlight App

## Introduction
Everyone deserves a chance to be in a career they aspire and can grow in. In the competitive job market today, under-represented communities often miss out on opportunities due to lack of facilities like training, education and career mentorship.  Diversity Cyber Council is a 501c3 Non-Profit that serves such demographics in the tech industry by facilitating several opportunities to establish a sustainable and diverse talent pipeline to the workforce. The vision is to enhance inclusion and representation in the tech industry through training, mentoring, networking, and visibility programs.

The Spotlight app project is being built with a goal to establish a sustainable and diverse talent pipeline that extends career equity to underrepresented demographics by providing access to competent training programs that lead to direct employment opportunities. The sustained effort to amass a coalition of nonprofits in order to address specific needs within the communities involves developing a centralized platform as the base of operations to collaborate, network and make a collective impact, thereby, illuminating possibilities.											

## Members

Josiah Bruner

Kevin Basista

Gagan Rajput

Sneha Kokil

## Business Requirements

#### Short-term
* Onboard non-profits and publish their offerings
* Onboard candidates and assess their needs
* Match non-profits to candidates
* Track candidate progress
* Track non-profit and candidate engagement
* Allow extracting operational and analytics reports

#### Mid-term 
* Automatic non-profit matching
* In-app scheduling capabilities
* Scale to onboard more offerings and non-profits 
* Allow non-profits to promote offerings

#### Long-term
* Provide automated suggestions for non-profit offerings
* Allow enhanced networking and group-sharing capabilities 
* If applicable, allow adding samples of offerings in non-profit content
   
## Our Strategy

Most modern applications today are built with smaller, nimble components that allow them to achieve speed, scalability and security in their operations. Looking at the goal with which Spotlight App Project is being built, extensibility is also going to be one of the important characteristics. Our strategy in designing the initial architecture for Spotlight is to enable key features that drive the main purpose of the project, pay deliberate attention to the security aspects and choose the architectural elements, such that they can support the changing, long-term needs.

## Architecture Solution

### High-Level Architecture
* [General Architecture](./GeneralArchitecture.md) - the general architectural idea.  

### Detailed Architecture

#### Actors, Actions and Significant Scenarios

* [Actors, Actions, and Significant Scenerios](./Brainstorming/Actors,%20Actions%20&%20Significant%20Scenarios.md) - the general architectural idea.  

#### Key Non-Functional Properties
In this section we describe the key non-functional properties of the architecture.

##### Scalability
We did a bit of research to ballpark our possible market in the future.


~1.54 million nonprofits registered with IRS in 2016: https://nccs.urban.org/project/nonprofit-sector-brief


Very hard to find data on how many people take advantage of non-profits. As a high bound, let's say 25% of the US takes advantage per year: ~82.375 million

Comparsison: LinkedIn has ~830 million users across 200 countries: https://about.linkedin.com/

So our scale is roughly one order of magnitude smaller than LinkedIn. This is still *very large* and the architecture proposed needs to be able to scale to this size.
##### Extensibility

Non-profits operate in a huge number of different causes and may collaborate in a near infinite number of ways. Although our initial design will support only a subset of these possibilities, it's clear that the platform needs to be extensible enough to support the growing number of non-profits and their needs.

#### Usability

We must be cognizant that both non-profits and candidate users may have very limited experience in technology. As such, our architecture focuses significantlly on ease-of-use and the ability for quick iteration and rapid prototyping. This will help UX and engineering teams to spend more time understanding user needs.


#### Capabilities
(Replace samples below with actuals)
* [Fridge Capability](./Key%20Capabilities/Fridge%20Capability.md)
* [Card and Payment](./Key%20Capabilities/Card%20and%20Payment.md)
* [Identity and Profile](./Key%20Capabilities/Identity%20and%20Profile.md)  
* [Kitchen Capability](./Key%20Capabilities/Kitchens.md)
* [Meal Inventory](./Key%20Capabilities/Meal%20Inventory.md)
* [Pricing](./Key%20Capabilities/Pricing%20policies.md)

#### Architecture Diagrams

#### Architectural Decision Records (ADRs)





