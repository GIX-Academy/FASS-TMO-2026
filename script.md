Good afternoon everyone. 
This is Benny Chin. The title here is "Everything happens somewhere, telling sotries with maps". In this session I would like to share something about maps. 

Next slide is just a very quick intro about myself. I am a geographer by training. I mainly teach Geographical Information Science (or GIS) courses and some programming courses in NUS. I am also working with some colleagues in Geography Department on a cross disciplinary programme called Geospatial Intelligence XDP (or GIX). We will come back to this programme later. In short, I am teaching computing in geography. 

Some may curious on why, and how geography is related to computing. And this is partly related to this topic---because everything happens somewhere, every event has a location, e.g., the transactions of alcohol products, the distribution of the EV charging consumptions; every movement has a path, like, how did you come to here, this LT11, today, we have quite a lot of audience here today so this must generate quite a large demand of transportation to get to this particular location, on this weekend time, which is not a normal pattern; every problem or issue has a geography, and if we want to understand the context, the underlying structure of the problem, so that we can solve it, we need to study the geography behind it. For example, disease, transport, housing and et cetera. And in this studying process, if we can get all the location data, time data, every stats or numbers in this phenomenon, we need some systematic and computational tools to help us explore the problem, and come up with a solution eventually. 

In the next few section, I will show you some examples. And the first example is related to something we do everyday, the human movement, which is also something that shapes the city. 

This is an image of a town, with a train station at the center, a open station plaza in front of it, some shops or shophouses that shapes the street blocks. There is also a community space and field at the top area. Although this is not a real place, it reflects a common pattern in Singapore, or a small town that has a MRT station and public space. Here, what is missing? So this is just an image of empty buildings and landscapes. We do not see any people or human activity in it yet. 

So, let's add some people and vehicles in it. We can see some people in the open plaza, some cars and buses moving on the streets, so we can expect there are some bus stops that may not be visible at this scale. This is what we are going to analyze, the human movement in a town. And it is 'complex' in a sense that it contains different types of events, different structure, and different objects. 

In geography and GIS, to analyze this kind of comoplex phenomenon, we will try to systematically split them into different layers, we call this process "explode" the data into different layers. Now we have one layer of streets, one layer of buildings, one layer of bustops and train stations, one layer of POI (point of interest), and on top we have a layer of the mobility/movement/interactions. After we split them into different layers, we can analyze or model them separately, or combine them using some computational approaches. 

Next, let's map the movement of people. There are some lines and arrows. Those in red or purple indicates high flows, blue means medium flow, and some not so visible grey arrows indicate low flow of people. These are the data that we can collect from easylink card, when you tap-in tap-out, a movement is recorded, or by counting the number of people or vehicle passing by some specific point of location. 

Then, we can further analyze the flows and distances, e.g., draw a 10-minutes walkable distance. Or 

Aggregate the flows into some higher level interactions, to show the so-called spatial interactions between places. This map not only shows the flow of people, but also the connections and interactions between places. 

Maps are not just about places, it can also shows relationships or interactions. 

If we expand the scale to a larger area, and analyze the interactions between places. Like here, on the left, we quantify the flows between places; in the middle, we can model them as a network, identify strong internal flows---what we called a community, then on the right we map them back to the city. 

If we apply this to the City state of Singapore, then we can identify some 'hubs', where commuters or the movement concentrated, and understand how people move between them. The next 2 slides are some maps from a real study, we used Singapore easylink data, and analyze the community changes in Singapore before and after COVID-19. 

Here is the Singapore communities before and after COVID-19. The north region and northeast region are very similar, but the Central, West and East Regions changed quite a lot. The most significant change is the central region, previously it is a large and strongly connected area; and it split to 3 smaller regions, indicating the flows become fragmented. 

The next two maps show the connections between these areas. 

So, what did this tell us? The first image shows the physical part of a town, but not the people. And when we add in the people, we can see how people move, and how the movement can change the structure of the city. Of cause, in this story, we focus on the movement. If you focus on other phenomenon, like greeneries, ecosystem services, health issues, aging, or air quality, then you will see a different set of patterns and maps with a similar analyzing process. Let's get back to the human movement part.  

What this story try to tell is that a city can change without being rebuilt. The physical part of a city can include the buildings, roads, stations, and land-use land cover, these are the structural part of a city. While these appear to be the most represented in many maps, e.g., if you open google map, or whatevery map, you will always see the roads and buildings, they are not the only things that we need to analyze when we look at a city. We also need to look at other aspects of human activities, for example the flow of a ciy, the trips and movements that we can 'measure' in a way; or we can try to understand the behavioural part of a city---things like the choices, routines, restrictions or adaptations of people. These patterns can change from time to time, and this is what we call a dynamic city. It is not dead or fixed; in a way, we can treat it as a living or organic thing. 

So, a map shows where things are. A network shows how places depend on each other---aka connected. Put them together, we can understand a city more deeply. 

Next, let's zoom in a little bit, and look at the NUS campus. The hidden geography of NUS. And see how everyday movement can create interaction and eventually lead to potential disease spread. 

This is a map of NUS. Ventus is here, this is a car park, and LT11 is a building near the LT13.   

This is an illustration of a building near the Central Library, called AS8. It is illustrated by ChatGPT so it is slightly different in real world. And now, it is just a physical part of the building. 

When we add some people in it, it becomes something like this. Some people sitting together to discuss their work, some walking around, some talking at the corridors, etc. 

In NUS, if you are a student or staff, you will likely be connecting the NUS Wifi with your devices. So in NUS, usually all floors or rooms will have a WIFI access point (or AP), and our devices will automatically connect to the nearest AP to maintain a stable connections. So, through the AP connection logs, we can identify which devices have 'visited' a floor. Then, we can identify who have been connected---by connected it means staying in the same room, or in the COVID term, close contact. 

This is a chart of the number of active staff (on top) and student (at the bottom) in a day (from hour o to 23). Different lines mean different days. One week of data is used. the two lines at the bottom are weekends. There are quite a lot of students in the campus after 6pm of weekdays, compared to staffs. 

Next, is a chart of interaction between staff, between student, and between all staff and student. 

Using the WIFI data, we can then generate a series of networks on close contact or physical connections. So that everyone is a node, and the interaction between them as link. And we can also convert this to a location network, where nodes are building floors, and links are the flows between places. 

And if we apply this to the campus...

These are the results for the location network. These are the community detection result, where the nodes are locations. The most important differences between staff and student is the clear separation beteween FOS and medical school building in staff, but for students they are all mixed. 

Next, this shows the connectivity between places. Different types of users have different patterns. 

Then, this naturally lead to a question we ask a lot in academic: so what? We don't need the wifi data to know that staff and student have different moving pattern. What can we do with this information? 

Let's look at this small story. There are some students discussing in group, one of the student, in blue shirt, is sick and coughing. Another student, in brown shirt, starts feeling seek. He is a hard working student, so he goes to a class despite feeling sick. And silently, the virus got spread to other classmates and the lecturer. Now the lecturer feel sick. Next, if the lecturer go to a class, then he will be spreading the disease to more students. 

With the individual contact network data, we can simulate this process. In every round, we can start the first case, the patient zero, or index case from any of the student, then expose the connected individuals to the virus and spread it, and in the next iteration, spread to the next connected peoples---the friends or friends. We can records the number of infected and infectious people at every simulated iteration, the time step; and we can record when a person is being infected in different rounds. 

This is a simulation result for 1000 rounds. The curves are quite typical as being simulated in other studies. From here, we can identify the time when the new exposed case reach the highest point, meaning that before this time-20, the number of newly exposed people keep increasing, until this point, then the number decrease. People exposed and infected before that time point can then be considered as early infected. 

Then, we can map out those places that are popular (i.e., visited a lot by) among the early infected people. The map shows that the risk is not evenly distributed. 

This story, in overall, we start from the movement of people within the campus, to a simulation of the interaction between people. Therefore, it is not a story about disease or a map, it is also about the geography of everyday campus life that show where people go, where people mix with each other, and how space shapes the contact and interaction. 

The previous two examples focus on human movement, but this is not the only field that we can apply the same analysis approach. One way of thinking, can apply in different phenomena. The thinking way is that, when we see a phenomenon, we gather relevant data, we analyze it, then we can map the story. 

Next you will see the six maps of different topics. From hazards and environments to animals and human activity. 

This map shows the wind speed near the East Asia---a super typhoon called Bavi that pass by Taiwan and hit Zhejiang China in early July. 

This is a map of the Pacific that shows the ring of fire (earthquakes). 

Next is a map of fire event within a month. Will you expect that fire event is something that happens that dense and frequent? 

Now, this is a map of seabird tracking---different colors means different types of species. and the points are the location of the birds. Before seeing this map, I wouldn't know that the oceans are so busy if you look at it from the birds' perspective. 

Compared to birds, this is the city night light---a map that can reflect the density of human activity. Because this is a map of city light generated from satellite image, it doesn't reflect the human activity beyond land surface.

So the next map is about the ship map. This shows that some locations are busier than other part of the sea or ocean. For example the Melacca strait, Hormuz Strait, and the Suez Canal. Different topics, different maps, and different stories. 

In the next section, I would like to talk a little bit on the lesson we can learn from the 'Computer Revolution' and discuss about AI. 

About 30 years ago, personal computer becomes more and more popular. And this led to a worry that computers may replace human work. But today, we can see that most jobs did not disappear---they include computers as part of the job. Back then, know how to use MS Office Word, Excel and Powerpoint are considered as competitive skills that you can write in your CV. Now, every office workers use computers, teachers use computers and projectors to teach. Computers are everywhere and blended into many of the jobs. 

If we group jobs by how they use computers in different levels:
Tier 1, the general computer user that use common tools like emails, web browser, and MS Office. 
Tier 2, the compputational proficieny users who use specialised software, like ArcGIS, AutoCAD (for architect), or Image/Video editing softwares. 
Tier 3, the computing profession, these are the people who develop the future computer---basically what the students in Computing Schools are trained for. 
Let's term the total of the three as computer-using or CU. 

This is a country map of Computer Using divided by total workforce. It basically shows the distribution of computer or digital literacy between countries. 

The next map shows the computing profession (tier 3) rates. The distribution are similar to the previous map, with some countries starting to decrease to second levels and some countries remain in the top group. 

This map in green, shows the Tier 3 divided by the total computer using group. And it shows a different pattern, that some of the countries in Affrica and India stands out as the high level group, whereas the US, some Europe countries, Australia and China becomes lower. This is because the base of those countries are small. 

Let's look at the numbers. In Singapore, the computer using percentage is 90%, very high compare to global average. But, if you look at the T2 ratio and T3 ratio (divided by total workforce) are 10% and around 6%. If you look at the global average, it is even lower at 5.4% ans 2.2%. 

What does this mean? It means the arrival off computers did replace some jobs, but it did not destroy the job market---rather it reshaped the employment ecosystem. Some jobs disappear, some jobs emerged, and many jobs changed. AI may follow a similar path. The question is, how and what will be the change?

Another thing is, in Singapore, around 90% of jobs are computer-using, but less than 10% are high-end core computing jobs. This means that there are large opportunities beyond the core computing industry. They lie across wider economy, where people can combine computing and AI with knowledge of the domain, e.g., geography, business, healthcare and many other fields. 

So in other words, the future is not only about working on AI, but also working with AI. Computer had become essential tools in almost every profession, and AI may become part of how many kinds of work are done. So, the future needs not only people who build AI, but also people who know what problems are worth solving with it, and how to do this.  

So, the key takeaway for you all is, learn to use AI beyond computing. Next, let me talk about the GIX Geography and FASS. 

What is Geography? If we put the answer to this question in simple words, it is one of the field that focus on real-world problems, literally, the problem or phenomenon of the real world itself. It is about the location, where it happens, about the people, who is affected, about time, how it changes, and about solution, what should we do next. Geography gives the real-world problems a place, a context, and a human meaning. 

In the following few slides, I will briefly talk about this programme, Geospatial Intelligence cross-disciplinary programme (XDP). GIX is a programme collaborated between Geography and School of Computing. If you go to website (the qr code or google this programme) you will see that some of the course codes start with CS, which means they were originally SoC courses. Geography gives the meaning on people, place, and environmentm; computing gives the thinking and practical skills on working with data, models, and systems. AI help detecting patterns and provide recommendation on solutions. Human judgement is the most important thing we want the student to learn---how to ask better questions and act responsibly. 

This is a screenshot of the introduction website for the GIX programme. This website shows four examples of the applications, including disaster managements (like volcanoes or typhoons); urban mobility (this example focus on the 15-minutes city), on promoting health (how to live healthier), and about EV and autonomous vehicles. 

GIX in a nutshell contains four main steps---4 main things you should learn. The two in the middle, data and analyze are basically the skills related to spatial thinking and computational thinking. The first and the last, care and act, are the other two important aspects beyond practical skills.  






