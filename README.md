# GinaVisnansky INFM600 October 17, 2017
### SQL Queries in Quarry

#### 1. Pages and Categories

1. https://quarry.wmflabs.org/query/22267
2. https://quarry.wmflabs.org/query/22268
3. https://quarry.wmflabs.org/query/22269
4. https://quarry.wmflabs.org/query/22270

###### In the first query, YvoRob joined the primary key, page_id from the page table with cl_from of the categorylinks table to pull a list of page names and the categories each page is linked to. The second and third queries join the page table with the categorylinks and pagelinks table and limit the results to category links labeled 'All_orphaned_articles'. However, the user did not limit the query to a small number of results, so the query failed when I ran it. By adding a limit of 10 and setting the select to 'distinct' the query runs successfully.  The fourth query pulls a list of page titles and their associated namespaces. Based on all four queries together, the user could be looking for pages that are tagged as orphaned articles. 

#### 2. Revisions

1. https://quarry.wmflabs.org/query/20530
2. https://quarry.wmflabs.org/query/15568
3. https://quarry.wmflabs.org/query/20756
4. https://quarry.wmflabs.org/query/20761
5. https://quarry.wmflabs.org/query/20762
6. https://quarry.wmflabs.org/query/20763

###### Drewmutt ran several queries from the revision and recent changes tables. Using different query methods, the user appears to have been looking for pages that were revised or changed recently. One method, though unsuccessful, attempted to select articles with the most recent revision timestamp via *select min(t1.rev_timestamp) ts*. Query 2 was ran successfully, but found no records where the revision comment is *like %i am the source%*. However, testing *like %update%* as a revision comment finds many records.

#### 3. Articles for Deletion

User's page https://quarry.wmflabs.org/SoWhy
1. https://quarry.wmflabs.org/query/20701
2. https://quarry.wmflabs.org/query/20804
3. https://quarry.wmflabs.org/query/20857
4. https://quarry.wmflabs.org/query/20862
5. https://quarry.wmflabs.org/query/21168
6. https://quarry.wmflabs.org/query/21063

###### Over the last two months, SoWhy ran 45 queries with the majority of them focusing on articles marked for deletion. The user ran queries to find the articles, the users who marked them, why they marked them based on revision comments, and when the articles were last revised. Searches involved the page, revision and logging tables. It's possible that this user was working in a collaborative effort to tag articles or find articles that have been tagged as potentials for deletion.


###### Word Count: 337
