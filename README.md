# Team 2 MIST4610Project1

## Team Name:
47114 Group 2

## Team Members:
1. Michael Chun [@hajirushi](https://github.com/hajirushi)
2. Teja Vegesna [@teja-vegesna](https://github.com/teja-vegesna)
3. Dylan Ladd [@DylanLaddUGA](https://github.com/DylanLaddUGA)
4. Michael Kushnerick [@michaelkushnerick](https://github.com/michaelkushnerick)
5. Pratik Patel [@PratikPatel4444](https://github.com/PratikPatel4444) 
6. Kyle O'Connor [@kyleoconnor5](https://github.com/kyleoconnor5) 

## Problem Description:
The task that we have been assigned is to build a relational database of our soccer club. While we as the audience may only see the players and the match, there are numerous factors behind the scenes that are responsible for the overall management of a soccer club. The central entity of our data model is the team itself, which works with other entities such as players, coaches, staff, sponsors, training, league and opponents as the core components allowing the team to function. We are interested in modeling the relationships between the numerous entities, as well as generating sample data for the attributes in our entities. We also are engaged in developing functional queries that will allow us to gather information on the club to allow for increased performance where the team may need it. 

## Explanation of our data model:

Our model is founded on the structure of all the major components that make up a soccer club. Starting off with the equipment entity, which contains a one to many relationship with equipment sessions. The equipment is vital for players to be able to train, but also vital for them to play in matches, such as shin guards and goalie gloves. This is demonstrated through a one to many 
relationship because there can be multiple sessions where one piece of equipment can be used.

Moving on to the training session entity which is connected to session equipment, team, and facility. All 3 of these relationships are demonstrated through a one to many relationship.For every training session, there is some sort of equipment that is being used, and this is represented in the one to many relationship between training sessions and session equipment. The one to many relationship with team is because one team can have multiple training sessions. Typically most teams hold multiple training sessions within one day. For this same reason, there is a one to many relationship between facility and training session, as multiple training sessions can occur within one facility. 

The team entity is connected to staff, players and training sessions, and all carry a one to many relationship. There are multiple members of staff who end up working for one team, which explains the one to many relationship. This includes janitors, coaches, equipment staff and so on. The team entity’s one to many relationship with players is due to the fact that there are singular teams that contain multiple players. 

The staff entity is also connected to the staff type entity, demonstrated by the one to many relationship. There can be many staff types that work for one staff. Example staff types like medical and training are separate, but they still both work for one staff. The staff entity is also connected to the physiotherapy session entity through a one to many relationship. A staff member can have multiple physiotherapy sessions. The physiotherapy session has a one to many relationship with players for the same reason, as one player can have multiple physiotherapy sessions.

The player entity is one of the central entities in the data model. Without the players, there cannot be a team. The player entity is connected to player stats, physiotherapy sessions, membership, team, and agent. Playerstats are connected to players through a one to many relationship, and this is because one player can have multiple types of player stats such as goals and assists. Between agents and players, there is a one to many relationship because it is possible for agents to have multiple players that they work for. There is a one to one relationship between players and membership. Players can only have one particular membership, there cannot be multiple memberships for one player, which is why this is highlighted as a one to one relationship.

Finally, there is the match entity which is connected to player stats and facility both through one to many relationships. There are multiple player stats that can be recorded during a singular match, which explains the relationship between these two. Match and facility also have a one to many relationship because multiple matches can take place in the same facility.


Picture of the data model:

![image](https://github.com/hajirushi/MIST4610Project1/assets/123567332/600cb642-9a95-4f2d-a9c6-d8bf5b29c2cf)


### Data Dictionary:
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/a1eaacbc-da48-4df0-ac85-913331a9a40e)
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/2cc07b17-9bfd-45e7-b73a-2af6f16874a2)
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/5bc5cc50-1b3d-4868-812e-08d7c5b43d62)
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/bdd22c07-7cb3-4af3-b1f8-14079d0d3c70)
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/1e080d7e-094c-4c20-9c0f-a444f403f791)
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/b24d260b-137b-4009-9709-3f613ca6fdf5)
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/4664cb04-2828-4835-a0b1-cc7c0885b4b5)

## Queries:
**Green = Complex**        **Yellow = Simple**
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/51d3efc8-40dd-438b-8610-9fa54adb5943)



1.) Query 1 lists the name of all the players that are present on the soccer team for the team “Puppies”. Along with all the soccer players' names is the position that each individual plays.

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/581c931c-624f-4c7a-8505-25116617ee64)

Query 1 allows the manager to get a grasp on this team as a whole. It allows the manager to accurately line up the name of the player with the position that they play. This can be crucial in the development of a soccer team. This data would be beneficial in areas such as injury management (which player would replace another), team chemistry (which players play best with each other), and strategic planning. All this data is fundamental for a soccer team to be successful.


2.) Query 2 lists physiotherapists first name and the amount of sessions that they participated in from the dates 1-1-2021 to 03-25-2023.

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/9bcab232-aa21-44d5-9ef8-9cda97d256d1)

Query 2 allows for the manager to see the most impactful and resourceful physiotherapists. This is valuable information that could be used in the hiring and firing process based on a team’s needs. By ordering the count in descending the manager can quickly analyze the number of times that a physiotherapist conducted a session. The data was pulled from a 2-year period to ensure that the data may not be inaccurate or misrepresentative of the value of the physiotherapist.


3.) Query 3 lists  the percentage of all training sessions that are advanced and further sorts  into the different equipment sets used for each training session. 

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/f6388979-be67-4ba3-b805-db7d53e022e5)

Query 3 allows team managers to get a grasp on which equipment sets are most frequently used, providing important information for budgeting and resource allocation. Since different skill levels have differing training schedules, it is also important to further filter by team skill level to better accommodate for the different teams needs. This will help save costs by focusing funds on the more frequently used sets. In addition, based on team performance, coaches can change up training sessions to focus on weak points found in matches.


4.) Query 4 lists out all staff members first and last names along with their phone number, teamName, and roles, it further sorts the staff members to show only the ones that work with the highest rated teams.

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/add79e7a-1a05-47f6-b0e2-41cc19dc19c2)

Query 4 givesthe manager a good overview of the staff. By providing the manager with the overview of a staff the manager can make important decisions about the staff (raises, firings, hirirngs etc.)


5.) Query 5 displays the amount of yellow cards and red cards that each player has obtained for the season if they have at least one 1 Yellow Card and less than or equal to 1 red card.

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/01f7293f-3922-4fc4-92ef-11acf86913af)


Query 5 would be useful to a manager of a soccer club because they would know which players they need to manage regarding discipline monitoring, player management and tactical considerations. If a player gets multiple yellows in a game then a player will get a red card resulting in their ejection for the rest of the match (and possibly half of the second match depending when the red card was given). By having access to a player's yellow and red card data it can help prevent a key player from being tossed out during an important match.


6.) Retrieve the details of players who are members and belong to teams with a skill level of 'Advanced'.

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/d9badf01-75e3-4b1c-becc-6c120a0befdc)

Query 6 would be useful because a  manager would be interested in retrieving the details of players who are members of teams with a skill level of 'Advanced' to identify top talent within the organization and ensure they are receiving the appropriate level of training and development. These players are likely the ones who contribute significantly to the team's performance.



7.) Query 7  lists the  playerID, player’s first and last name, what position they play, and the amount of goals and assists they have recorded if they have scored more than 1 goal and have more than 2 assists

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/7eefce37-f6bc-4543-9ca3-55c93a21f991)

Query 7 would allow the manager of the soccer team to see the potential of a player based upon their most important statistics (goals and assists). This data could be used in numerous circumstances, whether the manager is trying to recruit a player to join their team for the next season (phone) , or to establish a game plan against the player if they are on the opposing team. 


8.) Query 8 lists out the facilities that hosted matches between 2 different dates (2022-01-01 and 2023-01-01), and the number of matches played

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/5aeac634-60d4-4b20-9001-8bff01f71fa9)

Query 8 allows the manager to get an insight about where the matches will take place. The manager can then determine hotel and traveling expenses that are needed. Along with the frequency the manager can then use the location (facilityName) of the stadium and determine whether the game will be home or away.

9.) Query 9 displays the fee amount and the number of memberships that each fee amount has.

![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/c360a796-99a0-4a38-b663-087a7dda3e5d)

Query 9 is important because a manager might be interested in data that reveals the fee amounts and the corresponding number of memberships for each fee amount, to assess and refine the club's membership pricing strategy. This information can guide the manager in adjusting membership fees to better match the market demand, potentially increasing membership numbers and overall club revenue. It can also aid in financial forecasting and budgeting by providing insights into expected revenue streams from memberships.

10.) Query 10 displays the playerID, players name, player's DOB and agents name
![image](https://github.com/hajirushi/MIST4610Project1/assets/163002852/818b625a-d6fd-4adc-bf89-5b0a90bef9df)






## Database Information:
Name of the database: ns_Sp24_47114_Group2

Additional Information: Each query listed above is marked in the database using stored procedures which can be called using the following format - CALLTP_Qx (where x is to be replaced by the query number)
