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

As this is the first time that our team participated in the Katas event, our work here is inspired by previous winners: TheJedis2020 (https://github.com/TheJedis2020) and The Archangels (https://tekiegirl.github.io/Archangels/).

## Architecture Solution

### High-Level Architecture
* [General Architecture](./GeneralArchitecture.md) - the general architectural idea.  

### Detailed Architecture

#### Actors, Actions and Significant Scenarios

* [Actors, Actions, and Significant Scenerios](./Actors,%20Actions%20&%20Significant%20Scenarios.md) - the general architectural idea.  


#### Capabilities
* [Analytics Capability](./Key%20Capabilities/Core/Analytics.md)
* [Authentication Capability](./Key%20Capabilities/Core/Authentication.md)
* [Forum Capability](./Key%20Capabilities/Core/Forum.md)
* [Multimedia Storage Capability](./Key%20Capabilities/Core/MultimediaStorage.md)
* [Notification Capability](./Key%20Capabilities/Core/Notification.md)
* [Persistent Storage Capability](./Key%20Capabilities/Core/PersistentStorage.md)
* [Recommendation Capability](./Key%20Capabilities/Core/Recommendation.md)
* [Scheduling Capability](./Key%20Capabilities/Core/Schedule.md)
* [Assignment Capability](./Key%20Capabilities/Core/SearchAndAssign.md)


#### Architectural Decision Records (ADRs)

You can find a list of ADRs relevant to this proposal here: [ADRs](./ADRs)




