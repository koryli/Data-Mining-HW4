# Homework 4

## Q2: Market segmentation

### pre-process the data

### data normalization

In order to analyze the data intuitively, we first calculate the frequency of each category in every user's tweet so that the data can be normalized.

![image](https://user-images.githubusercontent.com/123770080/232599887-8ce7da2b-852b-4f52-a92a-d0e653f52b4d.png)

# outlier removal

We also remove 4 unwanted categories: chatter, adult, spam and uncategorized. Because categorized and spam tweets will interfere with our analysis of other data. Adult and spam tweets are what we don't want to include in our clusters.

(1) Chatter

(2) adult

(3) spam

(4) uncategorized

Then, removing rows.

## Correlated categories

To classify and analyze better, we check some categories which are strongly correlated. 

The categories that make the cutoff above the certain value:

<img width="242" alt="Screen Shot 2023-04-17 at 3 11 35 PM" src="https://user-images.githubusercontent.com/123770080/232600006-5687b423-28b1-4270-93c8-8ed50e6e6cda.png">

<img width="302" alt="Screen Shot 2023-04-17 at 3 10 43 PM" src="https://user-images.githubusercontent.com/123770080/232600067-f6b0dd85-32e3-4d6a-b340-23bdb4e4a001.png">





