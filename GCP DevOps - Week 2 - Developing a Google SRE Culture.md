# Week 2: Developing a Google SRE culture
## DevOps, SRE & Why They Exist!
* SRE: How to think about, measure and incentivize reliability!
* What are DevOps & SRE? What is DevOps, Why does it exist?

  **How can developers write code faster and more efficiently?**
  1. Hand off code to Systems Engineers: (Developers think less about infrastructure the code will run on!)
  2. Systems engineers want to focus on reliability and working more sustainably! 

**How Google defines DevOps?**
1. Reduce organizational silos: (increase & foster cross-collaboration)
2. Accept failure as normal
    

## SLOs with Consequences
Develop server level objectives with consequence, as the service of your applications relative to SLO’s wil guide business decisions.
  
### The Value of SRE to an organization
* SRE: protect, provide and progress software and systems *(focus on availability, latency, performance and capacity)*
	* Incentivized automation leads to → innovation
	* Launching and iterating  allow teams to → fail fast
* **==Postmortems==**: a blameless written record of an incident & root cause
	* ==**Pillars of DevOps methodology**==
		* Experienced SRE’s are comfortable with failure
		* Eliminate ambiguity with monitoring
		* Establish and document processes
	* ==**After an outage an SRE should**==:
		*  Seek to understand why it occurred
		*  How to prevent the incident from happening again
	*  ==**Components of a postmortem/retrospective**==
		*  Details of the incident
		*  Actions taken to mitigate or resolve the incident
		*  The incidents impact
		*  Its trigger and root cause
		*  Follow up actions to prevent its recurrence
	*  ==**Goal of a postmortem**==
		*  Ensure that the root cause are properly understood
			*  Issues/Root causes in isolation make not have triggered an outage, but combined lead to an incident
		*  Define and take effective action to prevent a recurrence
		*  Reduce the likelihood of stressful outages
			*  Improve systems 
			*  System hygiene
		*  Avoid multiplying complexity
			*  Remove the fixes/band aids on systems
		*  Learn from the mistakes
			*  What can be learned from past failure
    
### Blamelessness and Psychological safety
* Incidents are looked at objectively w/o designating a person or team as a root cause → leads to improved culture for teams
	* **Psychological safety:** people will not be punished or humiliated for speaking up (sharing ideas, concerns or mistakes)
		* Prevents stifled learning and innovation
	* **Building psychological safety**
		* Frame work as a learning problem and not an execution problem
		* Acknowledgment of personal fallibility
		* Model curiosity 
	* **Psychological safety = lead time, deployment frequency & time to restore**
		* Bridging is encourages
		* Cooperation is high
		* Messengers are not punished (even when sharing bad news)
		* Failure is treated as an opportunity for improvement
		* New ideas are welcome
	* **Blamelessness foster psychological safety**
		* Hindsight bias & discomfort discharge leads to blame
		* Hindsight bias: overestimation of the ability to predict an unpredictable outcome
		* Discomfort discharge: blame to release discomfort and pain
    

### SLOs & error budgets → break down silos
    

1.  What does reliable mean, and how is it being determined?
    

1.  Reliability: Good time/Total time = time the service is available & working
    
2.  Availability: Good interactions/Total interactions = users who experience a service that is working & available
    
3.  Service reliability: amount of reliability you re trying to reach & the amount of downtime you are willing to tolerate
    

3.  Error Budget = amount of unreliability you are willing to tolerate
    

1.  Measured uptime should be above target, error budget should have remaining (safe to push new feature releases)
    

1.  Error budget can also be spent on system changes, hardware & network failure, experimentation.
    
2.  Error budget helps prioritize engineer work. (Budget maintains balance between innovation and reliability)
    

5.  Service level objectives
    

1.  SLO: Precise numerical targets for system reliability
    

1.  Targets are agreed upon among stakeholders, sharing ownerships of reliability
    
2.  SLO performance indicates the reliability cost of new features/speed
    

3.  How to define SLOs for a service?
    

1.  SLI: service level indicator → how well are your service doing? (quantifiable measure of service reliability)
    
2.  SLI: (good events/valid events * 100%)
    
3.  SLI should map to use expectations (latency, quality, data processing, response time, throughput)
    

5.  SLO is the target for SLI aggregated over time.
    

1.  SLO should fall just below 100%, (99%-99.999%)
    
2.  SLO draws the line between happy and unhappy customers
    

1.  Anything below SLO = unhappy
    

7.  SLA is a promise about the health of your service to customers
    

1.  What is the business willing to do, if you fail to meet SLO (refunding money)
    

  
### Shared vision and knowledge
    

1.  Goals: unify vision, foster collaboration and share knowledge
    

1.  Unified vision: team vision statement 
    

1.  teams visions supports the company's vision
    

1.  Values: how can we achieve the vision (what guides behaviors)
    
2.  Purpose: why does the team exist (purpose & meaning)
    
3.  Mission: clear & compelling goals the team wants to achieve
    
4.  Strategy: how will we realize the team mission? (single initiative, leveraged, changes)
    
5.  Goals: what your team strives to accomplish, OKRS! (set ambitious goals)
    

3.  Collaboration & communication
    

1.  Should be high priority for SRE 
    
2.  Share common approach to platforms/solving problems
    
3.  Focus on problem-solving
    

1.  How SRE teams can communicate more effectively
    

1.  Service-oriented meetings: review the state of services
    

1.  Production changes, metrics, outage, paging events, actions items
    

3.  Team composition roles
    

1.  Tech lead: sets the technical direction of the team
    

1.  Review everyone's code, quarterly direction, build consensus
    

3.  Manager: runs performance management
    
4.  Project Manager: comments on design doc & writes code
    

3.  How knowledge sharing reduces organizational silos
    

1.  Cross-training: train team members to be flexible, schedule flexibility, boosts productivity improves morale, increases job satisfaction, reduces turnover & reduces costs
    
2.  Employee-to-Employee network
    

1.  G2g program
    
2.  Volunteer teaching network
    
3.  Helps peers learn new skills
    

4.  Job shadowing
    

1.  Expert knowledge & exposure to teammates
    
2.  Hands-on experience
    
3.  Opportunities to ask questions
    
4.  Conceptualize gradual change
    
5.  Cross functional collaboration
    
6.  Understand the nuances of a job role
    
7.  Pair team members to scale/retain knowledge
    

5.   Benefits of collaboration
    

1.  Real time collaboration
    
2.  Open commenting system
    
3.  Email notifications
    

  

6.  Module 3 exercise
    

  

## Make Tomorrow Better than Today

Introducing gradual change reduces the cost of a failure

  

1.  CI/CD: Continue integration, continuous delivery & canarying
    

1.  Continuous integration: Building, integrating & testing code within the development environment
    

1.  The goal is to work on code and test more often to increase code quality
    

3.  Continuous delivery: Deploying to production frequently
    

1.  Includes testing automation & deployment automation
    

5.  Software development as stages
    

1.  Agile development: Code & Build
    
2.  Continuous Integration: Code, Build, Integrate, Test
    
3.  Continuous Delivery: CI + Release & Build
    
4.  DevOps: owns the full pipeline
    

3.  How CI/CD reduced the cost of failure when implementing gradual change?
    

1.  Overcome agile transformation challenges
    
2.  Minimize code integration
    
3.  Reduce human error
    
4.  Code quality
    
5.  Automation
    
6.  Easy to recover if an error occurs
    
7.  Time to market is shorter
    
8.  More metrics/data points to review & act on.
    

5.  Canarying
    

1.  Deploying a change in a service to a group of users who dont they are receiving the change
    

1.  Evaluate the impact to the group
    
2.  Determine how to proceed if there are bugs (cheaper method opposed to rolling out software to a larger group of users)
    

3.  Canarying requirements
    

1.  Canary population should be large enough to representative subset of the control population
    

1.  Only differences between the population and canary group should be the production change! 
    

3.  Canary population should be small enough not to endanger the whole service if broken
    

1.  Should not take down the entire system if the service is broken
    

5.  Canary should not be overly complicated for those who monitor it
    

1.  Easy to understand how the canary impacts service health/easy to cancel if three is a problem
    

  

4.  Design thinking & prototyping
    

1.  Design thinking combines creativity and structure to solve complex problems.
    

1.  Five phases of design thinking
    

1.  Empathize → Observe/engage with users
    
2.  Define → Define the problem to be solved, from the POV of the user
    
3.  Ideate → Generate idea for solutions
    
4.  Prototype → Experiment with solutions
    
5.  Test → Test prototyped solution in the real world with users
    

3.  Importance of prototyping
    

1.  Without → fewer idear, slower failures, fewer successes
    
2.  With → more ideas are tested, faster failures, more successes
    

5.  Examples of prototyping
    

1.  Physical
    
2.  Paper drawing
    
3.  Clickable solution
    
4.  Role play
    
5.  Video recording
    

  

5.  Toil Automation
    

1.  Toil is a manual, repetitive, automatable, tactiona, no value system that scales linearly as the service grows
    
2.  Why is TOIL a problem?
    

1.  Career stagnation
    
2.  Low morale
    
3.  Confusion
    
4.  Slower progress
    
5.  Precedence
    
6.  Attrition
    
7.  Breach of faith
    

4.  Automation → what and how to automate
    

1.  Value of automation
    

1.  Consistency
    
2.  Platform → centralized to fix/test in a single place
    
3.  Quicker resolutions
    
4.  Faster actions
    
5.  Time Saved
    

  

6.  Psychology of change
    

1.  Personas
    

1.  Navigators → help success, encourage their behavior, use them as champions
    
2.  Critics → passion, energy 
    
3.  Victims → takes changes personally
    
4.  Bystanders → No idea what is going on, sticks to normal routine
    

3.  Emotions
    

1.  Denial
    
2.  Resistance
    
3.  Acceptance
    
4.  Exploration
    
5.  Commitment
    
6.  Growth
    

  

## Regulated Workload

1.  Measure reliability and toil
    

1.  Goals of measuring
    

1.  IT & business stakeholders can understand the status of  a service
    
2.  IT can analyze the data & identify the necessary actions to improve the status
    
3.  IT can make better decisions & impact across the organization
    

  

2.  Monitoring
    

  

3.  Goal-settings, transparency & data-driven decision making
    

  

## Apply SRE in your Organization
