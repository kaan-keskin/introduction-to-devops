# Introduction to DevOps - Part I

***Kaan Keskin, April 2021***

**DevOps** is short for **Dev**elopment and **Op**eration**s**.
It concentrates on collaboration between developers and other parties involved in building, deploying, operating, and maintaining software systems.

DevOps is a software engineering culture that unites the development and operations team under an umbrella of tools to automate every stage.

**DevOps is a set of cultural norms and technical practices that enable this fast flow of work from dev through test through operations while preserving world class reliability.** - Gene Kim

**DevOps blends lean thinking with agile philosophy.**

<img src="./images/IC-DevOps-Venn-Diagram.jpg" alt="DevOps Venn Diagram" style="zoom:20%;" />

## History of DevOps

Basically, the timeline goes something like this:

- Patrick Debois, a Belgian consultant, project manager, and agile practitioner is one among the initiators of DevOps.

- **2007**: While consulting on a data center migration for the Belgium government, system administrator **Patrick Debois** becomes frustrated by conflicts between developers and system admins. He ponders solutions.

- **August 2008**: At the **Agile Conference in Toronto**, software developer **Andrew Shafer** posts notice of a “birds of a feather” session entitled “**Agile Infrastructure**”. 

    Exactly one person attends: You guessed it, Patrick Debois. And he has the room to himself; thinking there was no interest in his topic, Andrew skips his own session! Later, Debois tracks down Shafer for a wide-ranging hallway conversation. Based on their talk, they form the **Agile Systems Administration Group**.

![10+ Deploys per Day: Dev and Ops Cooperation at Flickr](./images/10deploysperday.png)

- **June 2009**: At the **O’Reilly Velocity 09** conference, **John Allspaw** and **Paul Hammond** give their now-famous talk entitled “**10 Deploys a Day: Dev and Ops Cooperation at Flickr**”. Watching remotely, Debois laments on Twitter that he is unable to attend in person. Paul Nasrat tweets back, “Why not organize your own Velocity event in Belgium?”

    - [10+ Deploys per Day: Dev and Ops Cooperation at Flickr](https://learning.oreilly.com/videos/devops-in-practice/9781491902998/9781491902998-video169253) - 46 Minutes, June 23 2009

    - This presentation helped in bring out the ideas for DevOps and resolve the conflict of Dev versus Ops:
        - “It’s not my code, it’s your machines!”
        - "It’s not my machines, it’s your code!”
    
    - Traditional thinking:
        - Dev’s job is to add new features.
        - Ops’ job is to keep the site stable and fast.
    
    - **Ops’ job is NOT to keep the site stable and fast!**

    - **Ops’ job is to enable the business.**

    - **The business requires change, but change is the root cause of most outages!**

    - You have two options:
        - Discourage change in the interests of stability, or
        - **Allow change to happen as often as it needs to.**

    - **Lowering risk of change through tools and culture.**

    - **Ops** who think like devs, **Dev**s who think like ops!  

- **October 2009**: Debois decides to do exactly that—but first, he needs a name. He takes the first three letters of development and operations, adds the word “days,” and calls it **DevOpsDays**. The conference doors open on October 30 to an impressive collection of developers, system administrators, toolsmiths, and others. When the conference ends, the ongoing discussions move to Twitter. To create a memorable hashtag, Debois shortens the name to #DevOps. And the movement has been known as **DevOps** ever since.

- If you need to choose one author to learn DevOps culture and practices, you must read Gene Kim's books. My second suggestion is Jez Humble.

    - The Visible Ops Handbook, 2005
    - Continuous Delivery, 2010
    - The Phoenix Project, 2013
    - The DevOps Handbook, 2016
    - Accelerate, 2018
    - The Unicorn Project, 2019
    - Lean Enterprise, 2020

![Gene Kim Books](./images/gene-kim-books.png)

## Traditional Thinking

### Operations World

- Care About:
    - Everything is stable
    - Standards
    - Templates
    - Not getting bothered at 2:00 am

- Success:
    - Software is stable
    - Backup and restore works
    - Systems are operating within defined thresholds

### How Developers See Ops

![How Developers See Ops](./images/how-dev-see-ops.png)

### Developers World

- Care About:
    - Writing Software
    - Working Code
    - APIs
    - Libraries
    - Sprints

- Success:
    - Software Works - Laptop and Test
    - Finished Sprint

### How Ops See Developers

![How Ops See Developers](./images/how-ops-see-dev.png)

### Test Team World

- Care About:
    - Writing Test Code
    - Working Test Code
    - APIs
    - Frameworks
    - Sprints

- Success:
    - Test Works - Laptop and Testbed
    - Finished Sprint

### How Ops See Test Team

![How Ops See Test Team](./images/how-ops-see-test-team.png)

## Traditional Software Development Approach

### Traditional IT Service Delivery (Waterfall)

- Around since the 50s.

- Sequential Design Approach

- Requirements and scope are fixed.

![Traditional IT Service Delivery](./images/traditional-it-service-delivery.png)

### Challenges in the Traditional Approach

- Slow, manual, and error prone.

- The more complex a project becomes, the longer the schedule, and the higher the probability of scope and schedule surprises.

- **Waterfall Method:** Most of the development teams use waterfall method, which is time-consuming because of the larger size of the developer team, testers, and the code involved.

- **Productivity:** Codes that are large and bundled into release will result in jammed production and lower the productivity.

- **Difficult to Achieve Goal:** Less investment on resources and constant work make it difficult for the developers to achieve goal or an outcome.

- **Investment in Schedule Planning Systems:** More money is invested in schedule planning systems which are sensitive and inaccurate. As a result, it consumes more time to manage the systems.

### Before Agile Methodologies (Waterfall)

<img src="./images/before-agile-methodologies.png" alt="Before Agile Methodologies" style="zoom:60%;" />

## History of DevOps Methodologies

### Lean Management Philosophy

**Dr. William Edwards Deming (October 14, 1900 – December 20, 1993)** was an American engineer, statistician, professor, author, lecturer, and management consultant. Educated initially as an electrical engineer and later specializing in mathematical physics, he helped develop the sampling techniques still used by the U.S. Department of the Census and the Bureau of Labor Statistics.

Deming is best known for his work in Japan after WWII, particularly his work with the leaders of Japanese industry. That work began in July and August 1950, in Tokyo and at the Hakone Convention Center, when Deming delivered speeches on what he called "**Statistical Product Quality Administration**". 

Many in Japan credit Deming as one of the inspirations for what has become known as the **Japanese post-war economic miracle** of 1950 to 1960, when Japan rose from the ashes of war on the road to becoming the second-largest economy in the world through processes partially influenced by the ideas Deming taught:

- Better design of products to improve service
- Higher level of uniform product quality
- Improvement of product testing in the workplace and in research centers
- Greater sales through side [global] markets

Deming is best known in the United States for his **14 Points** (Out of the Crisis, by W. Edwards Deming, preface) and his system of thought he called the "**System of Profound Knowledge**". The system includes four components or "lenses" through which to view the world simultaneously:

- Appreciating a system
- Understanding variation
- Psychology
- Epistemology, the theory of knowledge

Deming made a significant contribution to Japan's reputation for innovative, high-quality products, and for its economic power. He is regarded as having had more impact on Japanese manufacturing and business than any other individual not of Japanese heritage. **Despite being honored in Japan in 1951 with the establishment of the Deming Prize, he was only just beginning to win widespread recognition in the United States at the time of his death in 1993.** President Ronald Reagan awarded him the National Medal of Technology in 1987. The following year, the National Academy of Sciences gave Deming the Distinguished Career in Science award. 

Books written by W. Edwards Deming and fellows:

- Statistical Adjustment Of Data, 1943
- Some Theory of Sampling, 1950
- Sample Design in Business Research, 1960
- Quality Productivity and Competitive Position, 1982
- **Out of the Crisis, 1982**
- The New Economics for Industry, Government, Education, 2000
- Statistical Method from the Viewpoint of Quality Control, 2012
- The Essential Deming: Leadership Principles from the Father of Quality, 2012

![Edwards Deming Books](./images/deming-books.png)

### Agile Manifesto
<>

### Lean and Agile in DevOps

- Lean: Management philosophy to eliminate waste across all aspects of business.
    - Derived from Toyota Production System

- Agile: Implementation of Lean for software development.
    - Short sprints

### Relationship Between Agile and DevOps

- Satisfy customer through early and continuous delivery of valuable software.
- Deliver working software frequently with a preference for the shorter timescale.
- Business people and developers must work together daily throughout the project.
- Replace non-human steps using tools.
- Improve the collaboration between all the teams.
- Automate to create a potentially shippable increment.

### Agile Project Management Example: Scrum

![Scrum](./images/scrum.png)

### Benefits of Agile Development

<img src="./images/benefits-of-agile-development.png" alt="Benefits of Agile Development" style="zoom:70%;" />

### Lean, Agile, and DevOps Combined

![Lean, Agile, and DevOps Combined](./images/lean-agile-devops.png)

### Extreme Programming (XP)

- Focuses on Software Quality and Responding quickly to changing customer requirements.

- Frequent releases and short dev cycles.

- Improve productivity and interaction with customer.

- Suggests:
    - Paired programing
    - Test Driven Development
    - Continuous Integration
    - Continuous Delivery

![Extreme Programming](./images/extreme-programming.png)

### Kanban

- Japanese for "Signal Board"

- 5 Core Principles:
    - Visualize the Workflow
    - Limit Work In Process
    - Manage Flow
    - Make Process Policies Explicit
    - Improve Collaboratively

![Kanban](./images/kanban.png)

### Putting It All Together

![Putting It All Together](./images/putting-it-all-together.png)



## Overview of DevOps - DevOps Phases

<img src="./images/devops.png" alt="DevOps" style="zoom:75%;" />

**DevOps is an agile relationship between development and IT operations.**

**The Development includes Plan, Code (Create), Build (Package), and Test (Verify).**

    - Plan: In planning, tools provide a repository for managing and storing various versions of a code. (JIRA, Git, Azure DevOps)
    
    - Code: Coding tools help in software design and the creation of software code. (GitHub, GitLab, Bitbucket,  Azure DevOps Repos)
    
    - Build: Build tools fetch the source code from the repositories and package them into executable applications. (Maven, Gradle, JFrog Artifactory, Docker, Ansible, Puppet, Chef)
    
    - Test: Testing tools help in continuous testing (manual or automated) to ensure optimal code quality. (JUnit, Selenium, Vagrant, TestNG, BlazeMeter)

**The Operations include Release, Deploy (Configure), Operate, and Monitor.**

    - Release, Deploy and Operate: Deployment and operation tools help manage, coordinate, schedule, and automate application releases into production. (Puppet, Chef, Docker)
    
    - Monitor: Monitoring tools help in continuous monitoring of released products. (Nagios, DataDog, Grafana, WireShark, Splank)

**Integrate: The heart of DevOps continuously automates the integration of all the different stages. (Jenkins, Azure DevOps)**

### DevOps Pipeline Example

![DevOps Phases](./images/devops-phases.png)

### Challenges in the DevOps Transformation

![Constantly Changing Challenges](./images/constantly_changing_challenges.png)

### DevOps Approach to the Challenges

- **Reduction in the code size delivery results in increased productivity.**

- **Smaller batch sizes, dedicated teams, and automated processes make scheduling simpler to operate.**

- **Batch sizes are divided into small cells. Each cell gathers its own data, reducing the size of the reports.**

- **Identifies productive and loss areas in the process. As a result, an organization can focus more on their goals.**

## DevOps Principles and Methodologies

### What Does It Take to Embrace DevOps? (CAMS)

![CAMS](./images/CAMS.png)

### DASA DevOps Principles

[DASA DevOps Principles](https://www.devopsagileskills.org/dasa-devops-principles/)

**DevOps is about experiences, ideas and culture to create high-performing IT organizations.**

Many definitions of DevOps exist, and many of them adequately explain one or more aspects that are important to find flow in the delivery of IT services.

**Instead of trying to state a comprehensive definition on our own, we prefer highlighting six DevOps principles we deem essential when adopting or migrating to a DevOps way of working.**

![DASA DevOps Principles](./images/dasa_devops_principles.png)

#### Principle 1 Customer-Centric Action

It is imperative nowadays to have **short feedback loops with real customers and end-users**, and that **all activity in building IT products and services centers around these clients**.

To be able to meet these customers’ requirements, DevOps organizations require the guts to act as lean startups that innovate continuously, pivot when an individual strategy is not (or no longer) working, and constantly invests in products and services that will receive a maximum level of customer delight.

#### Principle 2 Create with the End in Mind

**Organizations need to let go of waterfall and process-oriented models where each unit or individual works only for a particular role/function, without overseeing the complete picture.**

They need to act as product companies that explicitly focus on building working products sold to real customers, and all employees need to share the engineering mindset that is required actually to envision and realize those products.

#### Principle 3 End-To-End Responsibility

Where traditional organizations develop IT solutions and then hand them over to Operations to deploy and maintain these solutions, **in a DevOps environment teams are vertically organized such that they are fully accountable from concept to grave.**

IT products or services created and delivered by these teams remain under the responsibility of these stable groups.

These teams also provide performance support, until they become end-of-life, which greatly enhances the level of responsibility felt and the quality of the products engineered.

#### Principle 4 Cross-Functional Autonomous Teams

**In product organizations with vertical, fully responsible teams, these teams need to be entirely independent throughout the whole lifecycle.**

That requires a balanced set of skills and also highlights the need for team members with T-shaped all-round profiles instead of old-school IT specialists who are only knowledgeable or skilled in for example testing, requirements analysis or coding.

These teams become a hotbed of personal development and growth.

#### Principle 5 Continuous Improvement

**End-to-end responsibility also means that organizations need to adapt continuously in the light of changing circumstances (e.g. customer needs, changes in legislation, new technology becomes available).**

In a DevOps culture, a strong focus is put on continuous improvement to minimize waste, optimize for speed, costs, and ease of delivery, and to continuously improve the products/services offered.

Experimentation is therefore an important activity to embed and develop a way of learning from failures is essential.

**A good rule to live by in that respect is "if it hurts, do it more often".**

#### Principle 6 Automate Everything You Can

**To adopt a continuous improvement culture with high cycle rates and to create an IT organization that receives instant feedback from end users or customers, many organizations have quite some waste to eliminate.**

Fortunately, in the past years, enormous gains in IT development and operations can be made in that respect.

Think of automation of not only the software development process (continuous delivery, including continuous integration and continuous deployment) but also of the whole infrastructure landscape by building next-gen container-based cloud platforms that allow infrastructure to be versioned and treated as code as well.

**Automation is synonymous with the drive to renew the way in which the team delivers its services.**

## Overview of DevOps Tools

### DevOps Toolchains

![DevOps Toolchains](./images/devops_toolchains.png)

### DevOps Tools Example

To implement DevOps and work within the DevOps environment, the various tools required are:

![DevOps Tools](./images/devops-tools.png)

### Best Practices for DevOps

![Best Practices for DevOps](./images/best-practices.png)

### Security

Security should be part of the automated testing. It should be built into continuous integration and deployment processes during the migration to cloud-based platform.

### Proper DevOps Tools Selection

The Applications should be deployable on different environments (cloud or on-premise). 
In this way, you can pick and choose the best public or private cloud for the job.

![Proper DevOps Tools Selection](./images/proper-tool-selection.png)

### Requirements Tools

Tools are used to share the files and communicate within the team and other teams.

![Requirements Tools](./images/requirements-tools.png)

### Code Development Tools

![Code Development Tools](./images/code-development-tools.png)

### Artifact Creation Tools

![Artifact Creation Tools](./images/artifact-creation-tools.png)

### Testing Tools

![Testing Tools](./images/testing-tools.png)

### Packaging Tools

![Packaging Tools](./images/packaging-tools.png)

### Release Management Tools

![Release Management Tools](./images/release-management-tools.png)

### Configuration and Monitoring Tools

![Configuration and Monitoring Tools](./images/configuration-monitoring-tools.png)

## Agile and DevOps Example

![Agile and DevOps Example](./images/agile_devops_example.png)

The End!