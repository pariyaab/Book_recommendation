# Book_recommendation
It is a practical recommendation system (retrieval and ranking tasks) using TensorFlow Recommenders and Keras and deploy it using TensorFlow Serving.

##What is a recommendation system?!
A recommendation system ia a system that gives a query (context) which is what we know about the liking list, and filter the corpus (full catalog of items) to a shortlist of candidates (items, documents). A query (context) can be a user id, user's geographical location or user's history of previous purchases and the resulting candidates can be some new items that we guess are interesting for the user.

##Recommendation stages (tasks)
In practice, dealing with a large corpus and filter it to a shortlist is an intractable and inefficient task. So practical recommender systems has two (or three) filterng phase

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
