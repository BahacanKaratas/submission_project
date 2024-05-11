Problem 1
Problem: The tags are broken up into individual characters on the post view page.

Answer:
The underlying issue for Problem 1 was that the tags were not being handled correctly when creating a new article. Specifically, if the tagList was provided as a string, it was not being split into an array of tags correctly. Instead, it was being treated as an array of individual characters, which led to each character being displayed as a separate tag. This issue originated from the ArticleService class, where the create method was responsible for processing the tagList when creating a new article.

Problem 2
Problem: New tags are not shown on the home page under "Popular Tags", even after a page refresh.

Answer:
The underlying issue for Problem 2 was related to the way tags were being retrieved and displayed. The TagService's findAll method was not correctly fetching the tags or there was a caching issue that prevented new tags from being displayed immediately. This could be due to a caching mechanism on the server or client side that needed to be invalidated when new tags were created. Alternatively, it could be a database query issue where new tags weren't being included in the query results. This issue would originate from the TagService class, specifically the findAll method, which is responsible for providing the list of tags to the frontend.

For the full file, you would need to provide the specific ArticleService and TagService class files where the logic for creating articles and retrieving tags is implemented. If you have those files, I can insert the root cause explanations into the appropriate comments within the code.