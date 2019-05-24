# veil_of_ignorance

### Hosted on Heroku:
https://veilofignorance.herokuapp.com/

## Summary
What rules would we make for a society if we did not know which member we would be? More often than not decision makers have great ideas to help certain people, but the implementation of these ideas may not help the intended citizens.  This project seeks to build a virtual veil of ignorance: a tool allowing a decision maker to examine how their decisions will affect a specific member of a US state.  The application uses U.S. Census data to generates a probable citizen with demographic information according to each state's distribution of data (Education level, age range, ethnicity, and gender).  It also visualizes the distribution of data for each state while comparing it to the nation as a whole.

## Team Roles
One role was to access, clean, and load the Census data to the website; another to visualize the data with supplementary charts; a third to build the interactive map connecting each state to the correct data; and my role of hosting the website with Heroku, ensuring the appropriate library dependencies are up-to-date. 

## Individual Responsibilities
I built the logic for our application to "role the dice" to pick each demographic quality for a citizen.  Instead of having an equal chance of choosing each quality, the probability of choosing a quality matches the distribution of the state.  For example, if 30% of a state's citizens have bachelor's degrees, 10% have master's degrees, and 60% have high school diplomas as their highest degree of education, then our application has a 40% chance of choosing a citizen who has a degree from higher education. 

I also was in charge of hosting our website on Heroku.  A part of verifying our website worked as intended on the Heroku server was making sure other group members were aware of where the production data is stored.  One recurring issue was accessing the data using dynamic filepaths instead of absolute paths.  Helping members resolve these issues meant understanding the other roles enough to integrate each process seamlessly.  Through these endeavors I learned more about the connections between various programming languages (Python, Unix, HTML, CSS, JavaScript), frameworks (Flask, Jinja, D3.js, Plotly), and using asynchronous promises to ensure our application incorporated the data received from api calls.

## Challenges
Our interactive map was originally built with an older version of D3 which did not allow the use of promises. We restructured our code so that the data from the api calls could be used appropriately.  Unfortunately, we had to reuse code in several places, sacrificing modularity and efficiency in doing so.  As far as we can tell, the only fix for this is to rewrite our map using a modern version D3.

## Improvements
In the future, We would like to allow users to save a list of citizens that our application creates.  This would allow our users to further analyze the implementation of their ideas (e.g, running monte carlo simulations).
