
# A Journey into the Heart of Recommender Systems


#### Author : Chao Wang
#### Date: September 15, 2018



How does Amazon know what kind of books you may like to purchase and read?

How does Netflix know which movie to suggest you watch?

How does Yelp know which restaurant nearby you might want to visit?

Those companies use step-by-step recipes to figure out your preference based on the information you and other people offered to them. The recipe books are called recommender systems.

Where to get the recipes and how to use them? Well, let's take a simpler example to demonstrate how the recommender system works.






### Which Dish Would You Recommend?

Say I want to bring my new friend Sylvia lunch next week, and I noticed that Sylvia brought a stir-fry last week. If my options are sushi, burger, bibimbap and salad wrap, which one should I bring? What food would she like more?

![food](https://media.github.ubc.ca/user/1635/files/6861e044-b8e6-11e8-8e6f-37c4a512cd78)


|  |Sylvia's lunch: Stir-fry | Sushi | Burger | Bibimbap | Salad Wrap |
|---|---|---|---|---|---|
| Tempreture| Hot | Cold | Hot | Hot | Cold |
| Ethnic food| Yes | Yes | No | Yes | No |
| Rice-based| Yes |  Yes | No | Yes | No |
| Score | <span style="color:green">3 </span>| <span style="color:blue"> 2 </span> | <span style="color:blue"> 1 </span> | **3** | <span style="color:red">0 </span>|

First I select a couple of food features that identify her stir-fry. They are Food Temperature(Hot/Cold), Ethnic food (Yes/No), Rice-Based (Yes/No). All the criterias have boolean values. Say Sylvia's stir-fry scores 4, each same answer other dishes get, the dishes get one point. Let's take a look at their score. The highest scored dish shows the more similarity to Sylvia's Stir-fry. We assume the more similar the new dish is to her stir-fry, the more likely Sylvia is going to be happy. As we see, Bibimbap, the rice-based warm Koream dish is the winner!


Let's look at this problem from another angle. Not only I know Slyvia eats Stir-fry, I also know what Sabrina, Mani, Jack, and Socorro likes.

|   | Stir-fry| Sushi | Burger |Bibimbap | Salad Wrap |
|---|---|---|---|---|---|
|Sabrina|Yes | No | Yes | Yes| Yes |
|Mani| Yes |Yes | No| Yes | No |
|~~Socorro~~| ~~No~~| ~~No~~ | ~~Yes~~| ~~Yes~~ | ~~Yes~~ |
|~~Jack~~ | ~~No~~ | ~~No~~ | ~~No~~ | ~~No~~ | ~~Yes~~ |
|Sylvia| Yes |?|?|?|?|
|Vote | |1 vote | 1 vote |**2 votes** |1 vote |


We will see which friend(s) shows a similar taste of Sylvia and then I can bring the lunch the friend(s) likes.
Because Socorro and Jack don't like Stir-fry, they probably don't share the same taste with Sylvia, so I discount their opinions in the system. Mani and Sabrina are the two friends who's opinion matters. But they have some divided options on Burger, Sushi and Salad Wrap, they both love Bibimbap though. If we count all the votes from Sabrina and Mani, Bibimbap gets two votes, it is the winner again!
![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSksMv4qcb1_xm12zwyYLY0z2oVn4sb8V7lsuUBOIiShSZYHwEM)



The first recipe we used is called **content-based filtering system**, the second recipe is called **collaboratively filtering system**.
In short, a recommender system gathers your previous choice and other similar people's choices, and seek to give you a rating or prediction. So which one is better? and which one did Amazon, Netflix and Yelp use?

Well, they probably use both, which is called **Hybrid Recommender System**. The more info they take into consideration, the more likely you will take an action! It is said that the recommender systems usually bring 10-20% more extra revenues to the business.


## The Simplified Model

To simply the utility model of a Recommender system, it takes sets of customer opinions, and sets of item features and then give us a vote, rating or a score.

![screen shot 2018-09-15 at 1 48 00 pm](https://media.github.ubc.ca/user/1635/files/04ab8d04-b8ee-11e8-92e1-7d62a826c4e2)





### Does All Recommendations Come From Recommendation Systems?

However, not all the recommendations you see online are based on a recommender system. Here are some examples:

* Staff pick from Indigo.ca. That is simply an input from the company, it did not use your or other people's input.

* Most popular indie songs on Spotify. It is simple aggregates of the user actions.

* Personalized Emails. Interpersonal language will make you feel closer to the brand. A Back to School promotion email probably starts with "Hey (username), here is what we picked up for you for a new school year!"


Of course, those companies use more sophisticated recommender systems to figure out your preference, but you get an idea of how to make a decision. Maybe we can build a recommender system to help us choose a pub for our next MDS Saturday party?




### Reference:
1. [Recommender_system (Wikipedia)](https://en.wikipedia.org/wiki/Recommender_system)
2. [Lecture 41 — Overview of Recommender Systems | Stanford University](https://www.youtube.com/watch?v=1JRrCEgiyHM)
3. [Recommender Systems (Youtube)](https://www.youtube.com/watch?v=Eeg1DEeWUjA)

### Photo sources:
1. [Stir-fry rice](http://assets.kraftfoods.com/recipe_images/opendeploy/508968_1_1_retail-c652c0f882363f96444f291e789202b8058b650e_642x428.jpg)
2. [Sushi](https://img.grouponcdn.com/deal/5nqMiaVPQsLESRWCmMxPNQ/shutterstock_124581196-1500x900.jpg/v1/c700x420.jpg)
3. [Burger](https://www.seriouseats.com/recipes/images/2015/07/20150728-homemade-whopper-food-lab-35-1500x1125.jpg)
4. [Bibimbap](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Dolsot-bibimbap.jpg/1200px-Dolsot-bibimbap.jpg)
5. [Wrap](https://spicedblog.com/wp-content/uploads/2016/03/Thai-Peanut-Wraps4-600x400.jpg)
6. [Bibimbap Meme](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSksMv4qcb1_xm12zwyYLY0z2oVn4sb8V7lsuUBOIiShSZYHwEM)
