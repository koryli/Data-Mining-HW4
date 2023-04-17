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







