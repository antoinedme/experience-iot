
## Experience in deploying IoT technologies for elderly friendly Smart Cities.

Many city-dwelling elderly people can be greatly affected after a minor change in their living or health conditions. Also, nutrition and pollution became a major factor of health across the world. Metabolic diseases, quality of life (impairments) and respiratory disease are among the most common risks. 

Through the new wave of Information and Communication Technologies (ICT), Internet of Things (IoT) and Smart City systems, it is now possible to help individuals capture and make use of their personal data in a way that will help them maintain healthy and independent for longer. 

![Opening Antoine de Marasse](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/01-title.png) 

Contents:
- [How do we keep our elders safe and well within the community?](https://github.com/antoinedme/experience-iot/blob/master/README.md#how-do-we-keep-our-elders-safe-and-well-within-the-community)
- [Ubiquitous Service MAnagement and Reasoning archiTecture](https://github.com/antoinedme/experience-iot/blob/master/README.md#ubiquitous-service-management-and-reasoning-architecture)
- [Ontology and Semantic Web](https://github.com/antoinedme/experience-iot/blob/master/README.md#ontology-and-semantic-web)
- [Platform, services and Internet-of-Things](https://github.com/antoinedme/experience-iot/blob/master/README.md#platform-services-and-internet-of-things)
- [Poster: Singapore use-case](https://github.com/antoinedme/experience-iot/blob/master/README.md#poster-singapore-use-case)



### How do we keep our elders safe and well within the community? 

Three general parameters have been selected for observation, each one related to different activities detection:
- Socialization: place of interest visits, senior activity centre visits frequency, activities attended
- Mobility: physical activity, going-out frequency and going-out length
- Activity of Daily Living: meals frequency, sleep activity, vital signs.

The objectives of this technology deployments is done with the aim of:
- Keeping the elderly safe and well within the community while empowering caregivers with technology tools to help in their daily work
- Extending the living space for elderly, encouraging them to perform outdoor activities 
- Enhancing physical activity of the elderly using wearable technologies  

### Ubiquitous Service MAnagement and Reasoning archiTecture

The Ubiquitous Service MAnagement and Reasoning archiTecture (UbiSmart) platform makes use of standard commercialized sensors producing events, a gateway UbiGate that relays the structured event data to the main component – the Server written in Node.js. Eventually, notifications are sent to other devices as part of Service Provisioning. The reasoning is situated in the server: incoming events are stored in a database, translated in triples using Notation3 format and queued to be processed within the reasoning cycle. 

Different set of technology are deployed to fit better with the elderly needs and challenges:
- The indoor unobtrusive technology set is composed of 1 sleep mat, 2 contact sensors and 3 motion sensors. This set of devices enables the data collection of simple daily activities and processed them to the UbiSmart reasoning engine in order to extract meaningful information about Activities of Daily Living and lifestyle performances.
- Internet-of-Things and outdoor technologies: In order to involve more people in the projects, together with healthy elderly and active elderly population, the team developed internally an Android application that integrates an activity tracker data (Fitbit WebAPIs).

![Pilots Technology](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/03-technology.png)

### Ontology and Semantic Web

The ontology in the system has been created manually as well as the rules. They represent a common sense about observations (presence detection in a space, object manipulation) and implied conclusions based on past K=knowledge (the person is in the kitchen, preparing some food, receiving a visitor). 
- Abstract model: Static ontology describing the world that does not change (sensor type associated to its abilities and characteristics, type and description of detectable activities); 
- Instance model: Instantiated ontology comprising persisted information that was instan- tiated and has current information (e.g. sensor-room associations, durations of previously detected activity,… );
- Action: Injected knowledge produced by the sensors or a user interaction. 

Using the described knowledge base KB, the framework applies rules that conclude about what the current user’s activity is, computes new durations, updates the persisted information about this instance, and decides about notifications to be sent. The conclusions are passed to software components performing decided actions. The reasoning cycle ends and waits till next event triggering a new cycle. 

### Platform, services and Internet-of-Things

Different set of visualizations and tools are being implemented in order to provide more accurate and meaningful data. More importantly, the participants have access to some relevant data that impact their daily life such as climate and air pollution in the context of their geographical position and mobility context. 

![Final Sensors](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/04-sensors.png)

The app cross together different kind of data to help the user choose the most, context-aware, appropriate mobility solution, from active mobility (walk, bike, e-scooter) to passive mobility (bus and MRT). The data retrieved in the app are from the various sources:
- Fitbit Data (steps, distances, calories, sleep and vital signs data)
- Environment data (climate, air pollution, weather forecast)
- Places of Interests (healthy eateries, sport events, gyms, parks)

Following the user’s profile (age, gender, weight, height) and conditions (e.g. asthmatic, allergies, diabetic, disabled), the system will generate personalized recommendation of mobility together with necessary indications (locations of bikes, bus schedules, availability of e-scooters).

### Poster: Singapore use-case

![Poster](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/poster-iot-antoine-demarasse.png)

#### Creating pilot dashboard for Health
`var beacon_SACAntenna = new google.maps.LatLng(1.36459035, 103.85693395);
var beacon_BusStation3 = new google.maps.LatLng(1.362866, 103.855947);
var marker_blk406A = new google.maps.Marker({position: beacon_blk406A, map: map, animation: google.maps.Animation.DROP, icon: markerImageCC});`
![alt text](https://raw.githubusercontent.com/antoinedme/pilots_views/master/DataCollection-Map.png)

#### Risk models Calculator
Not activated in this version.
![alt text](https://raw.githubusercontent.com/antoinedme/pilots_views/master/Models-Algorithms.png)

#### Cohort Plot
Visualizing high-dimensional geometry and analyzing multivariate data for profile and survey data,
serving data from online CSV: https://github.com/antoinedme/SurveyPulseView1/blob/master/PULSEDATAVIEWIMT.csv
Available data parameters are:
- `age_group` Participant's age (years old)
- `bmi_score` Calculated (Body Mass Index), approximate measure of your total body fat
- `framingham` The Framingham Coronary Heart Disease Risk Score estimates
- `score` General Well-being Risk Score estimates
- `monthly_steps` Estimated wearable or declared physical activity
A point in *n-dimensional* space is represented as a polyline with vertices on the parallel axes; the position of the vertex on the i-th axis corresponds to the i-th coordinate of the point. 
Used for *statistical considerations* and *cohort identification/selection*.
![alt text](https://raw.githubusercontent.com/antoinedme/pilots_views/master/DataCollection-Cohort.png)

Using JS libraries:
`<script src="js/Chart.min.js"></script>`
`<script src="../vendors/jquery-sparkline/dist/jquery.sparkline.min.js"></script>`
`<script src="../vendors/Flot/jquery.flot.js"></script>`
`<script src="../vendors/echarts/dist/echarts.min.js"></script>`
`<script src="../vendors/echarts/map/js/world.js"></script>`


Antoine de Marassé https://www.linkedin.com/in/hiantoine/
