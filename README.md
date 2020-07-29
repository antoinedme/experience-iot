
## Experience in deploying IoT technologies for elderly friendly Smart Cities.

Many city-dwelling elderly people can be greatly affected after a minor change in their living or health conditions. Also, nutrition and pollution became a major factor of health across the world. Metabolic diseases, quality of life (impairments) and respiratory disease are among the most common risks. 

Through the new wave of Information and Communication Technologies (ICT), Internet of Things (IoT) and Smart City systems, it is now possible to help individuals capture and make use of their personal data in a way that will help them maintain healthy and independent for longer. 

Direct link to the poster: https://github.com/antoinedme/experience-iot/blob/master/README.md#poster-singapore-use-case


![Opening Antoine de Marasse](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/01-title.png) 

Workshop's contents:

1. [How do we keep our elders safe and well within the community?](https://github.com/antoinedme/experience-iot/blob/master/README.md#how-do-we-keep-our-elders-safe-and-well-within-the-community)
2. [Smart Living Framework](https://github.com/antoinedme/experience-iot/blob/master/README.md#smart-living-framework)
    1. [Ubiquitous Service MAnagement and Reasoning archiTecture](https://github.com/antoinedme/experience-iot/blob/master/README.md#ubiquitous-service-management-and-reasoning-architecture)
    2. [Ontology and Semantic Web](https://github.com/antoinedme/experience-iot/blob/master/README.md#ontology-and-semantic-web)
3. [Platform, services and Internet-of-Things](https://github.com/antoinedme/experience-iot/blob/master/README.md#platform-services-and-internet-of-things)
    1. [Creating pilot dashboard for health](https://github.com/antoinedme/experience-iot/blob/master/README.md#creating-pilot-dashboard-for-health)
    2. [Integrating Risk models](https://github.com/antoinedme/experience-iot/blob/master/README.md#integrating-risk-models)    
    3. [Data Plot and visualisations](https://github.com/antoinedme/experience-iot/blob/master/README.md#data-plot-and-visualisations)    
4. [Poster: Singapore use-case](https://github.com/antoinedme/experience-iot/blob/master/README.md#poster-singapore-use-case)


### How do we keep our elders safe and well within the community? 

Three general parameters have been selected for observation, each one related to different activities detection:
- Socialization: place of interest visits, senior activity centre visits frequency, activities attended
- Mobility: physical activity, going-out frequency and going-out length
- Activity of Daily Living: meals frequency, sleep activity, vital signs.

The objectives of this technology deployments is done with the aim of:
- Keeping the elderly safe and well within the community while empowering caregivers with technology tools to help in their daily work
- Extending the living space for elderly, encouraging them to perform outdoor activities 
- Enhancing physical activity of the elderly using wearable technologies 

### Smart Living Framework

#### Ubiquitous Service MAnagement and Reasoning archiTecture

The Ubiquitous Service MAnagement and Reasoning archiTecture (UbiSmart) platform makes use of standard commercialized sensors producing events, a gateway UbiGate that relays the structured event data to the main component – the Server written in Node.js. Eventually, notifications are sent to other devices as part of Service Provisioning. The reasoning is situated in the server: incoming events are stored in a database, translated in triples using Notation3 format and queued to be processed within the reasoning cycle. 

Different set of technology are deployed to fit better with the elderly needs and challenges:
- The indoor unobtrusive technology set is composed of 1 sleep mat, 2 contact sensors and 3 motion sensors. This set of devices enables the data collection of simple daily activities and processed them to the UbiSmart reasoning engine in order to extract meaningful information about Activities of Daily Living and lifestyle performances.
- Internet-of-Things and outdoor technologies: In order to involve more people in the projects, together with healthy elderly and active elderly population, the team developed internally an Android application that integrates an activity tracker data (Fitbit WebAPIs).

![Pilots Technology](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/03-technology.png)

#### Ontology and Semantic Web

The ontology in the system has been created manually as well as the rules. They represent a common sense about observations (presence detection in a space, object manipulation) and implied conclusions based on past K=knowledge (the person is in the kitchen, preparing some food, receiving a visitor). 
- Abstract model: Static ontology describing the world that does not change (sensor type associated to its abilities and characteristics, type and description of detectable activities); 
- Instance model: Instantiated ontology comprising persisted information that was instan- tiated and has current information (e.g. sensor-room associations, durations of previously detected activity,… );
- Action: Injected knowledge produced by the sensors or a user interaction. 

Using the described knowledge base KB, the framework applies rules that conclude about what the current user’s activity is, computes new durations, updates the persisted information about this instance, and decides about notifications to be sent. The conclusions are passed to software components performing decided actions. The reasoning cycle ends and waits till next event triggering a new cycle. 

### Platform, services and Internet-of-Things

#### Creating pilot dashboard for health

Different set of visualizations and tools are being implemented in order to provide more accurate and meaningful data. More importantly, the participants have access to some relevant data that impact their daily life such as climate and air pollution in the context of their geographical position and mobility context. 

![Final Sensors](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/04-sensors.png)

The app cross together different kind of data to help the user choose the most, context-aware, appropriate mobility solution, from active mobility (walk, bike, e-scooter) to passive mobility (bus and MRT). The data retrieved in the app are from the various sources:
- Fitbit Data (steps, distances, calories, sleep and vital signs data)
- Environment data (climate, air pollution, weather forecast)
- Places of Interests (healthy eateries, sport events, gyms, parks)

Following the user’s profile (age, gender, weight, height) and conditions (e.g. asthmatic, allergies, diabetic, disabled), the system will generate personalized recommendation of mobility together with necessary indications (locations of bikes, bus schedules, availability of e-scooters).

#### Integrating Risk models

We use several well known risk assessment models such as the The Framingham Heart Study and the Epidemiology of Cardiovascular Diseases (https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4159698/) and Verlato asthma risk assessment models.

![alt text](https://raw.githubusercontent.com/antoinedme/pilots_views/master/Models-Algorithms.png)

In the repository: https://github.com/antoinedme/pilots_views

![alt text](https://raw.githubusercontent.com/antoinedme/pilots_views/master/DataCollection-Map.png)

#### Data Plot and visualisations

The main drive for the validation of data collection and the project is to answer the following questions:
- How to assess the relevance and feasibility of the project?
- Are we building the right product/service at a citizen and city level?
- What has been the level of engagement of pilots’ partners? 
- How is the ecosystem reacting to the project? How to measure this support?
- How to measure users’ participation, engagement and acceptance?

In order to go through a strong validation assessment, we need to understand the duality of the project, as seen as the two main project end-users: the participants engaged within each pilot city (involved in data collection through the apps and questionnaires) and the local ecosystem, partners and local stakeholders such as communities, health departments, transport agencies and multiple kind of partners that can make use of the data and tools insights. 

In order to do so, we created dashboards for the data visualisations and visual exploration.

In general, all pilots have used validation guidelines that cover the following key aspects targeted in different capacities depending on the user (e.g. citizen / Policy makers - Public Health / Community leaders) and corresponding systems being validated:

- Functionality: to check if the technology performs all the necessary functions.
- Usability: focused on the way they are offered.
- Acceptance: how the users are using the technology (Fitbit; PulsAir app; dashboard).
- Engagement: concerns how easily they are to adopt and use it and share the aims and outcomes of the PULSE project and feel involved.
- Effectiveness: concerns how useful the project is perceived to be and if the participants show willingness to change behaviour?
- Empowerment: what impact does the PulsAir app messages’ have on the participants; does this self-awareness have an impact on their behaviour?

Using JS libraries (on bootstrap): `chart.min.js`, `jquery.sparkline.min.js`, `jquery.flot.js` and `echarts.min.js`.

![alt text](https://raw.githubusercontent.com/antoinedme/pilots_views/master/DataCollection-Cohort.png)

In this project validation, we want to evaluate the impact of the urban context on the participants Quality of Life (QoL). To do so, we use city data (air quality, mobility data, sensors data, neighborhood data), personal data (user profile, chronic diseases, activity data, lifestyle, conditions) and other external data and models results. Example of available data parameters are: `age_group` Participant's age (years old), `bmi_score` Calculated (Body Mass Index), approximate measure of your total body fat, `framingham` The Framingham Coronary Heart Disease Risk Score estimates, `score` General Well-being Risk Score estimates, `monthly_steps` Estimated wearable or declared physical activity.
Find the code in this repository: https://github.com/antoinedme/urban-repository

![alt text](https://raw.githubusercontent.com/antoinedme/urban-repository/master/Pilotswidgets-screenshot.png)

### Poster: Singapore use-case

To sum-up, please find this poster:

Abstract. Healthcare & well-being needs a revolution - and it is needed now. In the coming years, the relationship between people and digitized systems is going to change due in large part to the adoption of ambient technologies in daily life and to the considerable development in AI (Artificial Intelligence). This includes emerging 5G technologies, small medical devices, non-invasive new sensing technologies, collaborative robots (e.g. Amazon Echo, Google home, etc.), Internet-of-Things (IoT) applications, and secured data exchange mechanisms (e.g. Blockchain). Over the next 20 years there will be demographic shift from predominantly younger populations to older ones. Current models of care and pathways need to be trans-formed to become more citizen focused as well as to support greater com-munity resilience and sustainability. This will require different approaches to innovation in information technologies to improve quality of life for people as they age, to reduce onset of frailty as well as to better support those with long term conditions employing self-management and prevention strategies. This paper describes on-going project between NUS, IMT, HDB (Housing Development Board), and AXA Insurance, and aiming at pre-serving patient health and avoid deterioration of their quality of life (and also of their families) by fully utilizing disruptive information & communication technologies. Additionally, the goal is to help improve the quality of life of citizens while reducing the health-care expenditure. 

Presented by:
Antoine de Marassé1, Mounir Mokhtari1, Martin Kodys2, and Hamdi Aloulou3
Research groups:
- 1 Institut Mines-Telecom (IMT), France/ National University of Singapore (NUS)
- 2 University Grenoble Alpes, France/ IPAL
- 3 University of Monastir, Tunisia/ Institut Mines-Telecom, Paris, France

![Poster](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/poster-iot-antoine-demarasse.png)

Contact me via Linkedin:

Antoine de Marassé https://www.linkedin.com/in/hiantoine/
