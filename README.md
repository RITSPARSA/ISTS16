# ISTS16
February 2nd - 4th, 2018.

## Infrastructure Setup
### Infrastructure Configuration
https://github.com/RITSPARSA/ISTS16-InfrastructureConfiguration

This is an ansible repository that was set up to build the desired topology. The most reuseable part of this repository would be the network-setup role, which will automatically set static IP addresses for teams based on a dictionary. This repository will be maintained, polished, and added to for future years.

### Infrastructure Provisioning
https://github.com/RITSPARSA/ISTS16-InfrastructureProvisioning

This is a repository that was used to allocate the initial vm's that the competition used.

### Management Bootstrap
https://github.com/RITSPARSA/ISTS16-ManagementBootstrap

This was a quick ansible repo used to rapidly configure any machines that White Team used for management.

## Web Applications

### Command Center
https://github.com/RITSPARSA/ISTS16-CommandCenter

This web application was run off of the Raspberry Pi's, and gave teams insight into the various aspects of the competition. It also included buttons that would run ansible playbooks from this repository: https://github.com/RITSPARSA/ISTS16-AnsibleServer. 

### ECommerce
https://github.com/RITSPARSA/ISTS16-ECommerce

This site served as the primary place for teams to spend their credits and to earn money from successful checks. If this was down, teams would have to make purchases at the physical service desk.

## White Team Backend

### White Team Tools
https://github.com/RITSPARSA/ISTS16-WhiteTeamTools

This was a quick command line tool that White Team used to manage various aspects of the event. Included nice features such as tab completion, and was rapidly implemented using Google's fire library.

### White Team Central
https://github.com/RITSPARSA/ISTS16-WhiteTeamCentral

This was a backend API that centralized information about the competition, including credits, king of the hill information, ship counts, etc. The Command Center web application pulled it's data from this, but it also served as the backend for the WhiteTeam tools repository.

### ECommerce Backend
https://github.com/RITSPARSA/ISTS16-ECommerceBackend

This was a backend API for the ECommerce web application. It used the auth server for authentication, and managed teams credits.

### Auth Server
https://github.com/RITSPARSA/ISTS16-Auth

This was an API that both web applications in the competition used to authenticate with (Command Center and ECommerce). This means that both used the same pair of credentials to log in, and that you could have logged into any other team's infrastructure using your own credentials.

### Ship API
https://github.com/RITSPARSA/ISTS16-ShipAPI

This was another backend API used to keep track of team ship counts.

### Inject Server
https://github.com/RITSPARSA/ISTS16-InjectServer

This repository was intended to serve as an "auto-reply" inject server to easily serve the next stage in the questline to teams. We did not get a chance to test it before the competition, and therefore it was not used. However, it still may be useful for the future.

## Service Scoring

### Scoring Engine
https://github.com/RITSPARSA/cyberengine

This was the traditional scoring engine used for the competition.

### Service Checks
The following repositories contained checks used for the competition. They often involved some custom logic that tied into the White Team backend (i.e. Jenkins increments ShipAPI counters, ECommerce adds credits to teams)

https://github.com/RITSPARSA/ISTS16-ECommerceCheck

https://github.com/RITSPARSA/ISTS16-ScoringChecks

https://github.com/RITSPARSA/ISTS16-JenkinsCheck

The above Jenkins check ran builds from the two following public repositories:

https://github.com/RITSPARSA/ISTS16-Vega

https://github.com/RITSPARSA/ISTS16-Wolf



