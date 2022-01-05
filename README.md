# ScorpTest

### Repo Structure:
1) Scorp Backend Q1.ipynb: This notebook contains the solution to the first coding problem. Dummy data were created in order to test out the logic of the code provided.

2) Scorp Backend Q2.ipynb: This notebook contains the solution to the second coding problem. Dummy data were created in order to test out the logic of the code provided.

##### Logic for Question 1:

Here, we were asked to get the post details using the post_ids provided, assuming the posts exists. Once obtained we are to check if the user requesting for the posts liked any of them, if true return a struct_post instance of the post with the liked attribute set to true.

##### Logic used:
1) Query the Post table using the post_ids, if post does not exist return None.
2) For the existing posts, query the Like table to see if there is any instance where the user_id and the post_id exists. If True, it confirms that the requesting user liked a post.
3) For every post create an instance of the struct_post and populate the attributes of the struct_post with their respective values. If the requesting user liked any of the post set the liked attribute to True, else False.
4) Return the list of struct_post.


##### Logic for Question 2:

In this section we are provided with a list of post lists, and asked to return the a list of post. We are to use the created_at value to sort the list in descending order, if there are duplicates of the created_at value, we are to use the id of the post to sort. If there are duplicated Ids, we are to drop one (assumption made is that post with the 
same ids have the same content).

##### Logic used:
1) Map the created_at value to the post instance using a dictionary
2) If the created_at value already exists in the dictionary(hence, duplicated) switch to the ids and compare. If the id of the post already in the dictionary is lower 
than the new post id, ignore, else replace the post with the new one.
3) Once completed, convert the dictionary keys to a list and sort (descending order).
4) Create an output list and populate with the posts using the sorted keys.
5) Loop through the list finally to remove duplicate ids using a set as a monitor.
6) Return the final list of post


#### Tech Stack used to implement solution:
1) Python Programming Language
2) SQLAlchemy


Question 1 and Question 2 can be found here: [Click Here.](https://docs.google.com/document/d/1AA7IxfXNK6xQh5uUBn3qGRC8kUI5FTalPa47hxN370Y/edit)




