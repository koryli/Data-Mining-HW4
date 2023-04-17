# Homework 4

## Q1 Clustering and PCA

For both PCA and clustering algorithm of 11 chemical properties can distinguish the reds from the whites, as the graphs shows. 

### PCA

For PCA I choose pc1 and pc2 because it can explain 0.932 of the total compositon. And the graph shows that we can distinguish clearly the reds from the whites.
But it's hard for us to distinguish wine quality with PCA.

![image](https://user-images.githubusercontent.com/123716487/232603382-be5822e9-7670-4300-8a97-9a2d1c6d2d54.png)

![image](https://user-images.githubusercontent.com/123716487/232603554-05c9d931-0229-41b9-8327-d3a467780452.png)

### Clustering

For clustering algorithm, I use k_mean in clustering, and I use code to find the best number of cluster which is two. Then I draw the graph, it shows that we can roughly distinguish wine color with cluster, but there still some point which locate in cluster2 but the color is white. Also it's hard for us to distinguish wine quality with cluster.

![image](https://user-images.githubusercontent.com/123716487/232604994-0a091c20-2f7b-40c8-9eb6-4e24903f211b.png)

![image](https://user-images.githubusercontent.com/123716487/232605107-abefacb7-6f26-4493-8add-a2acb14fa425.png)


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

Component 1:

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

##  Q3

To get the rules that make sense:

First, we may have the concept of "lift","support" and "confidence"

Support: This measures how frequently the items in the rule appear together as a percentage of all transactions. For example, if the support for a rule {beer} -> {red wine} is 0.05, it means that 5% of all transactions contain beer and red wine together.

Confidence: This measures the proportion of transactions containing the antecedent (left-hand-side) of the rule that also contain the consequent (right-hand-side). For example, if the confidence for a rule {beer} -> {red wine} is 0.6, it means that 60% of the transactions containing beer also contain red wine.

Lift: This measures the strength of the association between the antecedent and the consequent, taking into account the support of both the antecedent and the consequent. A lift value of 1 indicates no association, while a value greater than 1 indicates a positive association, and a value less than 1 indicates a negative association. For example, if the lift for a rule {beer} -> {red wine} is 2.0, it means that beer are twice as likely to be purchased with red wine than they would be if there were no association between the items.

### Top 30 rules sorted by lift
![image](https://user-images.githubusercontent.com/112587000/232615690-9aa1a848-08bc-4fb2-a7ae-9fa93cab96a7.png)

It's not clear enough to see the rules that most make-sense.

First of all, sort the rules by confidence

![image](https://user-images.githubusercontent.com/112587000/232615964-61974e71-3bc9-43ad-bac2-1a9f2646ca67.png)

The rhs with the highest confidence were all whole milk. That means the people who come to buy food at the groceries will tend to buy milk.

Next, sort the rules by lift

![image](https://user-images.githubusercontent.com/112587000/232616152-2649e9e0-9a70-4891-968b-ea1e0f9e0f7b.png)

We can see good complements here: white bread and ham are very likely to be eaten together

![image](https://user-images.githubusercontent.com/112587000/232616203-5980affe-e559-4e0d-aef3-d1b0780de043.png)

while whole milk is the most frequent item, so the rules with whole milk may not have much informations because most people will buy it no matter they buy what other items.

![image](https://user-images.githubusercontent.com/112587000/232616303-7b280ed3-3c20-4a5d-adb5-810288a8cb9d.png)

![image](https://user-images.githubusercontent.com/112587000/232616320-40f61caf-40fc-4fff-be0c-7be564ea110c.png)

We can see that there is a negative relationship between support and lift.

![image](https://user-images.githubusercontent.com/112587000/232616360-57fadd9c-97cf-4937-afe9-c4ede851225b.png)

The two key plot indicates that when the order increases, the support increases and confidence decreases.

![image](https://user-images.githubusercontent.com/112587000/232616506-1f2f5f50-f84b-4baa-8607-358cc1317de1.png)

We want some more useful results, so we choose a relatively high confidence and support to include the item rules that are general and highly corralated 
These rule contains the items that are relatively bought frequently and they have high relationship. 
In these rules, we can even imagine the most popular dishes from these products. Like beef stew with potatoes, berries dipped in sour cream. But most of the rules are still not so interesting in my opinion, because they are too common.

We lower the support, just like what we do the above

there are 85 rules left.

We can see if a person buys red wine, they are more likely to buy other wines. If a person buys vegetables, they are also more likely to buy other vegetables. This is the routine operation of a person who comes to the groceries with a purpose and a preference.

{rolls/buns,shopping bags}=> {sausage}   
{beef} => {root vegetables} 
{root vegetables}=> {beef}
{ham}=> {white bread} 
{white bread} => {ham}              
{sliced cheese}  => {sausage}          
{berries} => {whipped/sour cream}

There are also some interesting rules that can be treated as recipes: If someone buys rolls,buns and shopping bags, they are likely to buy sausage, and what we said above: beef and potato(root vegetable), Berries with sour cream, chocolate waffles...We can come up with recipes that people like to eat, according to these rules.


















