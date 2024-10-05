---
title: Database-Driven Restaurant Recommendation Website for Jeonju
date: 2024-05-01
image:
  focal_point: "top"
---

I developed a website introducing hidden gems in Jeonju.
The project aimed to collect data on approximately 80 local restaurants, allowing users to discover and explore various dining options.

**Database Design and Implementation**
To support features like recommendation boards, restaurant information, and user reviews, 
I designed and implemented a database composed of three main tables: recommend_board, restaurants, and reviews.

**User Interface and Experience**
At the top of the home screen, there is a search bar for restaurant names, 
a section to explore restaurants by neighborhood, 
and another section to browse by food type. Below that, 
there are sections for adding restaurants and a recommendation board.

For example, if a user selects Jungwasan-dong, they will see a list displaying 
each restaurant's name, food type, and menu. Similarly, 
if they choose Japanese cuisine in the food type section, 
they can view a screen that shows the name, location, and menu for each restaurant.

Clicking on a specific restaurant brings up a detailed screen, such as for 
"Kung Pao Shrimp." This screen provides the restaurant's location, category, 
menu, a brief introduction, and photos of signature dishes. 
Additionally, there is a feature for reading and writing reviews below. 
Clicking the review button leads to a screen where users can rate and comment.

**Additional Features**
I implemented a recommendation board section that allows users to write posts 
recommending their favorite restaurants to others. 
Furthermore, I added a restaurant addition feature where users can enter 
restaurant names, locations, food types, characteristics, and descriptions, 
along with uploading images to add new restaurants.

**Software and Development Environment**
- Front End: CSS, JavaScript, HTML
- Back End: Express
- Database: MySQL