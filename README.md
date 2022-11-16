# Book_recommendation
It is a practical recommendation system (retrieval and ranking tasks) using TensorFlow Recommenders and Keras and deploy it using TensorFlow Serving.

## What is a recommendation system?!
A recommendation system is a system that gives a query (context) which is what we know about the liking list, and filters the corpus (full catalog of items) to a shortlist of candidates (items, documents). A query (context) can be a user id, the user's geographical location, or the user's history of previous purchases, and the resulting candidates can be some new items that we guess are interesting for the user.

## Recommendation stages (tasks)
In practice, dealing with a large corpus and filtering it to a shortlist is an intractable and inefficient task. So practical recommender systems have two (or three) filtering phase

    1. Retrieval (Candidate Generation)
    2. Ranking (Scoring)
    3. Re-ranking or optimazation or ...
    
 ## Representation of a query or a candidate

A query or a candidate has lots of different features. For example a query can be constructed by these features:

    customer_id
    customer_id_history
    etc.

And a candidate can have features like:

    item_description
    item_title
    item_price
    posted_vote
    etc.

These obviouse features can be numerical variables, categorical variables, bitmaps or raw texts. However, these low-level features are not enough and we should extract some more abstract latent features from these obvious features to represent the query or the candidate as a numerical high-dimensional vector - known as Embedding Vector.

To involve side-features as well as ids while learning latent features (embeddings), we can use deep neural network (DNN) architectures like softmax or two-tower neural models.
YouTube two-tower neural model uses side-features to represent queries and candidates in an abstract high-dimentional embedding vector.

## Book dataset

The book dataset is a benchmark dataset in the field of recommender system research containing a set of voting given to book by a set of users, collected from the amazon_us_review website.
