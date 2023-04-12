# NLP--Facebook-Post-Classification
## Background
As one of the largest social media websites in the world, Facebook is an attractive platform for businesses to reach their consumers. Almost all consumer-facing businesses have virtual presence on Facebook, in the form of Facebook business pages (e.g., see here for Target's Facebook business page). Everyday, Facebook users who visit these business pages generate a large amount of posts. These user posts may represent customer complains, questions, or appreciations directed towards the focal businesses.

For businesses, these user posts contain valuable information about customers' needs and preferences, and understanding what the user posts are talking about represents an important opportunity to get to know your customers in real-time.

## Dataset and Task
Dataset: A labeled dataset named "FB_posts_labeled.txt". It is a tab-delimited file with the following fields:
postId: this is a unique identifier for each user post. There are 7961 posts in total;

message: this is the text of each post;

Appreciation: this is a binary (0/1) indicator of whether a post is an appreciation;

Complaint: this is a binary (0/1) indicator of whether a post is a customer complaint;

Feedback: this is a binary (0/1) indicator of whether a post is a customer feedback (e.g., questions and suggestions).

Appreciation, Complaint, and Feedback are the three mutually exclusive content categories / classes in this dataset. They were labeled by humans, and the labeling isn't perfect (i.e., there may be ambiguous cases where the labels are not appropriate). However, for the sake of this assignment, let's treat them as the ground truth. 
Task: Build a text classifier to predict the content category of a post based on its textual content.
To evaluate the out-of-sample performance of your model, I use it to make predictions for 2039 posts in an unlabeled dataset named "FB_posts_unlabeled.txt". It is also a tab-delimited file, but only has postId and message fields. I keep the ground truth labels for these posts in a private place, in order to objectively evaluate model's performance. The performance metric will use is averaged F-measure across the three categories.

## Model Strategy

BERT

BERT stands for Bidirectional Encoder Representations from Transformers. It is a language representation model, which means it takes raw text and generate a meaningful representation (e.g., embedding) of it. It was developed by Google in 2018. With everything we have discussed so far, you are ready to make sense of all the key components of BERT:

1. Bidirectional means that, during training, the input sequences and its reverse sequence are both used;

2. Encoder Representations means that the model is aiming to generate representation of the input sequence, i.e., it acts like an encoder;
 
3. Transformers means that BERT uses a transformer architecture with self-attention.

## Result

<img width="927" alt="image" src="https://user-images.githubusercontent.com/92591719/231573400-945dfaf2-eca8-47e4-9ad7-4b10fc6a2cda.png">
