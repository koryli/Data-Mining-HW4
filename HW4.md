# Homework 4








## Q2: Market segmentation

### pre-process the data

### data normalization

In order to analyze the data intuitively, we first calculate the frequency of each category in every user's tweet so that the data can be normalized.

![image](https://user-images.githubusercontent.com/123770080/232599887-8ce7da2b-852b-4f52-a92a-d0e653f52b4d.png)

### outlier removal

We also remove 4 unwanted categories: chatter, adult, spam and uncategorized. Because categorized and spam tweets will interfere with our analysis of other data. Adult and spam tweets are what we don't want to include in our clusters.

(1) Chatter

(2) adult

(3) spam

(4) uncategorized

Then, removing rows.

### Correlated categories

To classify and analyze better, we check some categories which are strongly correlated. 

The categories that make the cutoff above the certain value:

<img width="242" alt="Screen Shot 2023-04-17 at 3 11 35 PM" src="https://user-images.githubusercontent.com/123770080/232600006-5687b423-28b1-4270-93c8-8ed50e6e6cda.png">

<img width="302" alt="Screen Shot 2023-04-17 at 3 10 43 PM" src="https://user-images.githubusercontent.com/123770080/232600067-f6b0dd85-32e3-4d6a-b340-23bdb4e4a001.png">

We select the correlation that is more than 0.6 and we think there can be 11 pairs to compare.
Here are several cluster we will focus:

1. Health lifestyle

Personal_fitness & health_nutrition. This pair has the highest correlation. And health_nutrition and outdoors also have a high correlation of 0.608. Thus, the first cluster is about people who care about health. 

2. college_uni & online_gaming

This pair has a very high correlation of 0.773, which should be of interest to college students.

3. Fashions

Beauty, cooking and fashion are very correlated with each other. These people will pursue a more fashionable and exquisite life.

4. politics & travel

Maybe people who like traveling and socializing will fall in this cluster.

5. parenting, religion & sports_fandom

The people who care about these things seem at the middle age.

### clustering by KNN

![image](https://user-images.githubusercontent.com/123770080/232600482-5690484a-ded2-4b27-9025-e250d3ccc1d0.png)

Because there is no clear result. Then, we will use k range from 3 to 6 to cluster, which can help classify the groups based on tweets preferences.

### PCA

We will only use the first two components.

### PCA & KNN comparison

KNN for 3, 4, 5, 6 clusters:

![image](https://user-images.githubusercontent.com/123770080/232600705-bb5d3b9d-123c-432d-abfc-88373922374c.png)
![image](https://user-images.githubusercontent.com/123770080/232600739-e2850f2c-6351-4b8b-aa48-1dc67a97de3a.png)
![image](https://user-images.githubusercontent.com/123770080/232600759-5ed2dbd2-80ff-4ec9-b9f8-3ec1f04a679e.png)
![image](https://user-images.githubusercontent.com/123770080/232600774-0069c887-e449-4f36-a59b-01e0d8a68772.png)

PCA: 

Component 1

[1] "religion"      "sports_fandom" "parenting"     "food"          "school"       
[1] "personal_fitness" "fashion"          "health_nutrition" "photo_sharing"   
[5] "cooking"         

Component 2:

[1] "politics"    "travel"      "news"        "college_uni" "chatter"    
[1] "food"             "cooking"          "outdoors"         "personal_fitness"
[5] "health_nutrition"

C1 & C2:

![image](https://user-images.githubusercontent.com/123770080/232601103-b2b9f9ad-2cbe-4042-80b7-dee425efe342.png)

Based on the graph, the clusters are similar with our assumptions. The following is our customer segmentation of the market and some advice for the drink company.

### 1. Health lifestyle

Personal_fitness & health_nutrition. These two are very close to each other. Outdoors is also close to these two on PC1. They may be fitness enthusiasts, athletes, health coaches, or nutritionists, who are passionate about staying physically fit, maintaining a healthy diet, and enjoying outdoor activities.

The beverage company could focus on promoting the health benefits of their products. For example, if the beverage is low in sugar and calories, high in vitamins and minerals, and made with natural ingredients, the company could highlight these aspects in their advertising to appeal to health-conscious consumers. Also, the company could collaborate with fitness influencers, health coaches, or nutritionists who have a strong social media following among the target audience.

### 2. young college student

Young college students, whose tweets include a lot of college_uni & online_gaming things, also tweet something about shoppping, tv_film.

The company could create a marketing campaign that targets the energy and focus benefits of their product. College/university students and gamers often require sustained energy and focus to get through long study or gaming sessions, and a beverage company could highlight the energizing and focus-enhancing properties of their product.

### 3. Fashions

Beauty, cooking and fashion fall in a young age area where the people who care about healthy life also fall. 

To advertise to these people, the company could create content that appeals to the target audience's interests. For example, they could create recipe videos that feature the beverage as an ingredient or develop a beauty routine that includes the beverage as a refreshing beverage to enjoy during a self-care routine. Besides, they could highlight the hydrating properties of the beverage and how it can help maintain healthy skin.

### 4. People who care about world and current events.

Politics, travel and news fall in one cluster. People who like traveling and socializing seem interested in these topic. 

The company could create a marketing campaign that aligns with the values and interests of the target audience. If the target audience is interested in social justice issues, the company could highlight their commitment to diversity and inclusion. They could create travel guides that highlight local cafes or bars where the beverage is served, or publish articles that discuss the politics of the beverage industry.

### 5. Middle-aged parents

parenting, religion & sports_fandom

Family, school and food also fall in this cluster.

This demographic is likely to prioritize health and nutrition, so the company could highlight the nutritional value of the beverage, such as its vitamins or antioxidants, could be an effective approach. Then, the company could sponsor events related to parenting, religion, sports, school, or food. For example, they could sponsor youth sports teams or religious conferences. 






















