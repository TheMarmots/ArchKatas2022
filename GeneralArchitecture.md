# General Architecture

<Insert diagram>

# Overview

# Architectural Characteristics

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