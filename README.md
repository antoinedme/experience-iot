
## Experience in deploying IoT technologies for elderly friendly Smart Cities.

Many city-dwelling elderly people can be greatly affected after a minor change in their living or health conditions. Also, nutrition and pollution became a major factor of health across the world. Metabolic diseases, quality of life (impairments) and respiratory disease are among the most common risks. 

Through the new wave of Information and Communication Technologies (ICT), Internet of Things (IoT) and Smart City systems, it is now possible to help individuals capture and make use of their personal data in a way that will help them maintain healthy and independent for longer. 

![Opening Antoine de Marasse](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/01-title.png) 

How do we keep our elders safe and well within the community? 

Three general parameters have been selected for observation, each one related to different activities detection:
- Socialization: place of interest visits, senior activity centre visits frequency, activities attended
- Mobility: physical activity, going-out frequency and going-out length
- Activity of Daily Living: meals frequency, sleep activity, vital signs

**The UbiSmart platform** makes use of standard commercialized sensors producing events, a gateway UbiGate that relays the structured event data to the main component – the Server written in Node.js. Eventually, notifications are sent to other devices as part of Service Provisioning. The reasoning is situated in the server: incoming events are stored in a database, translated in triples using Notation3 format and queued to be processed within the reasoning cycle. 

Different set of technology are deployed to fit better with the elderly needs and challenges:
- Indoor monitoring for the more frail ones (and/or homebound): motion sensors for each living space, contact sensors for smart objects, sleep mat with vital signs monitoring features)
- Outdoor Monitoring for the more active one: lifestyle using wearable Internet-of-Things technology

![Pilots Technology](https://raw.githubusercontent.com/antoinedme/experience-iot/master/img/03-technology.png)

The ontology in the system has been created manually as well as the rules. They represent a common sense about observations (presence detection in a space, object manipulation) and implied conclusions based on past K=knowledge (the person is in the kitchen, preparing some food, receiving a visitor). 
- Abstract model: Static ontology describing the world that does not change (sensor type associated to its abilities and characteristics, type and description of detectable activities); 
- Instance model: Instantiated ontology comprising persisted information that was instan- tiated and has current information (e.g. sensor-room associations, durations of previously detected activity,… );
- Action: Injected knowledge produced by the sensors or a user interaction. 


Using the described knowledge base KB, the framework applies rules that conclude about what the current user’s activity is, computes new durations, updates the persisted information about this instance, and decides about notifications to be sent. The conclusions are passed to software components performing decided actions. The reasoning cycle ends and waits till next event triggering a new cycle. 

Different set of visualizations and tools are being implemented in order to provide more accurate and meaningful data. More importantly, the participants have access to some relevant data that impact their daily life such as climate and air pollution in the context of their geographical position and mobility context. 



