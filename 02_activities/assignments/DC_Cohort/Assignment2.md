# Assignment 2: Design a Logical Model and Advanced SQL

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

#### Submission Parameters:
* Submission Due Date: `November 12, 2025`
* Weight: 70% of total grade
* The branch name for your repo should be: `assignment-two`
* What to submit for this assignment:
    * This markdown (Assignment2.md) with written responses in Section 1 and 4
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
    * One .sql file 
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pulls/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [x] Create a branch called `assignment-two`.
- [x] Ensure that the repository is public.
- [x] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [x] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.

***

## Section 1:
You can start this section following *session 1*, but you may want to wait until you feel comfortable wtih basic SQL query writing. 

Steps to complete this part of the assignment:
- Design a logical data model
- Duplicate the logical data model and add another table to it following the instructions
- Write, within this markdown file, an answer to Prompt 3


###  Design a Logical Model

#### Prompt 1
Design a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. 

Additionally, include a date table. 

There are several tools online you can use, I'd recommend [Draw.io](https://www.drawio.com/) or [LucidChart](https://www.lucidchart.com/pages/).

**HINT:** You do not need to create any data for this prompt. This is a conceptual model only. 

#### Prompt 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

#### Prompt 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2? 

**HINT:** search type 1 vs type 2 slowly changing dimensions. 

```
1. Type 1 slowly changing dimensions (overwrite changes): If the customer already exists than the changed address (column) will be updated.
The history of the old address will not be saved. 
2. Type 2 slowly changing dimensions (retain changes): The old address wil have a end-date now and a new row with the new address will be added.
![Tables_example](https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&dark=auto#R%3Cmxfile%3E%3Cdiagram%20name%3D%22Page-1%22%20id%3D%22eoebsmCHAySjbejiEOs3%22%3E7Z1bk6I4FIB%2FTVfNPDhFQFAfW9uZ3a2ZranpqZp9TUtUtpGwELvb%2BfWbQFAxQVHjrTlVXaWEEOGcL%2BFckvSdM5i9fUlwPP1GfRLe2Zb%2Fduc83Nk2atse%2FxAli7yk07PygkkS%2BLLSquAx%2BE1kYVFtHvgkLVVklIYsiMuFIxpFZMRKZThJ6Gu52piG5V%2BN8YQoBY8jHKqlvwKfTfPSrmutyv8gwWRa%2FDKy5JkZLirLgnSKffq6VuQM75xBQinLv83eBiQUwivkkl%2F3ueLs8sYSErE6F%2FS%2BkGGn%2Fc%2F34eAXen76OfwdWL9ayM2becHhXD6xvFu2KEQwSeg8ltVIwsibTvD4qahuqTeGlo%2FLOSF0Rliy4FVkQ215hSSkEO3rStx2Ac10TdTLiliqeLJseSUF%2FkUKYh%2Bh7JYJV2Ysvsrn7qcMJ0zSa%2FFjLhWGg4gk%2FBhlx2GI4zTIpZTVmAah%2FxUv6JwV7RRH%2FTG%2FWjaGPH5cKfx1IW%2FRryp6KWunrqztU8na3lPWP0QX6k9pEvwWIg6lNDfln74GsxBHvG9if6OoT7OxKL8qoc9kQEMq9BREU5IEQv6MxrJGSMZMfn2ijNGZPEikbCytbv2Exj9xMiFFlXEQhsXPRDQSxMQ0iFgmTbfP%2F7h8B9Yn987lTzzgx2h1zP9E9YQNaMTvmGMlmiU4Za8kNYyLnpZdeHScE9HhKHQM5inXAu9XtvXnQyUq%2FEFZgMMfYmCKJlkPnbJZKDvj6zRg5DHGI1H1lb%2B38g67Noxtg4NywY7DbCSfBr5PIr1%2B92Moo4EkwxeSQ4GMqtXeqdZeZz%2BtysZWAt67NRzy540w4%2F1xHvmpgsryPg%2Bnp72NnnvfT0iaAkJHIfRWVvg6A55Romq0dgaiVGtpELAFMGSCIdRzVIje47Dkgclz%2FSbPoozHTguofSILqKPAgmC4qadZ7zCrZ4smDxheNlo7w%2FDS1QwvXshy3QbP%2FKa9iThCNmfbGlA%2BjvDPR8bL8UxAET2lcSb4%2FCp%2BE%2BULixN%2B8LJZlMY4KrHp%2FTcX8Y3%2BEx49izhC5LdGOTH3IpKT4Cgt9NjPggnLc6EQYsvHyfOHZPL0QQwWvLT4%2BJh%2FijO26%2BYH618%2BfszvSv58cZ9t19t85uUzZrdefhxeXHpI6HdH9Ls9TcXDu2GN1s7QDXuqqZhjBxAdD1FtW%2FHWB%2FMiDA7G4g0Yi6itjm3njZchNXRdzQuMOJqu1rwoGVJD8Pd9YUYNpiSSVhIQdAxBDQuSIU3UPkMJKDJAUWPCZEgN3xd%2BmRC21s0UJ1pppgbhQ6JO%2FKb1A38uYvHQSAxvg4c1dy9vucLf46pku%2BEsoygB0zCHuYfLcXwYEQETLxCwBCMc3ssTMw5s1hsyv5kUdtoRZFUkg2Uzne4nV0ELOY5Kg3OqbLCr0%2Fk2c1dj2l4g9b5jfgMqT3DoXjzp7taY9QFexdm8ipz6K0q7u2qKAvLuhyi2YsB9769uV81aQObdNEQN8ypcNa8BuXdjFDXGq3DVuDyYPtdn%2BlxL%2Bt1T4%2B%2BQf6%2Br295h1s%2Bt52w8NQiv5p0BoWMQalgu2VND9JBMNodRY7LJnhqZB%2BPnao2fy6eTPTUcWw0MjDmavta82I%2BnxpYhnWyUoIYFfjxNMBrSyaYoakzgx1Nj0gpCxJ%2BQR3nILYApndAIh8NV6UYqdlXnK81ULlT3L2FsIXWH54yW%2Bct%2FU%2FxQpRqLAAOdJyOy5YmK5fCF6bOvmZGQELPgpXwjxm2IXg25n3mFuVN72fPJlpj3dLP0t1niGqv7WtaY5xquNGMvv8a8BzHfa3J7cvavKN293LMD8t1HavbAiO%2Bt2xbIUkO%2BkPA2TVHD%2FB5kaaK%2BkPE2hVFjHB9kQdT3Fsyfa0l5I0uN%2BkLOu6ZyZWdrXtIbWbo5xbDuHNadX77vNWy2ALI0EXOYLmAOpMbMF0BWjeAtmI7XYjpefsIAstS4djUxMOzoelsTw2dqgB7mDJhlqGnBM83GKTBrwBxHzYmeabZU2XsZenf7MnTRfIOWoVfli69nGTrS7Imy3e7V2LhXvw7d8dTMfAd1VTnbvZPZi5q9QsDBuOD%2BVjn4W01QLSIn3NFq6y7ekJuvr9rdkWnUbpt8hddq7izvcM2%2B3ZCeNw3S24bWSyTYZsGq0dxZwNJEWiFFbwwlu%2BtpUHqfY5SjvueG4zG%2FaTFDV818PQqDh1d%2F4HcFaaNTQtjWTGB9txCqzu42CDdTt8PIByTPgKTb0b1i3yeSCFJQN%2BEhVk9f0juMJ5u%2BhNQUFExfqq3d3Sko%2FchwcKq7VnNnGWjUJJQ6VQkwOgqjvV3EI7Cq0dxZdtfWJKJgMo45lur7iLc%2FRDlqHOsvHLUs1LKt5b8ZBqKOJKq%2Bw%2FcOiFITXX%2FTFz5qCaJcIMoMUfX9tXdAVKeSGnDPLu6e6aYInjmh54B%2Fdrh6nUP9s9sPBDmqfwbbKhrGqIEpvDb4ZydlqUk5vLaaPgFr2jhRTUrIFaPkGlEPZNRyUKvXK7a1AaKOJapJ%2BTRbN58ZHLZrddiWu2JdzmGz1TGoGhkYeXTdrZEOm63O7YZVXWYpaqC%2FZmvmg8PCLmMoNcldc9TZu48kZi27K%2Fw1eMcZQqpJ%2FpqjvvPAXzNOVKP8tRr%2Fq%2FW29q0u9j7euXF1pW9Ue%2Bfq7NL7JMGLtQrSD1y1%2FF0UrOhyOuV1km15%2FLlmfVfumrIiIb8Dw5GhGisnr4iLY5WoSt0pS932NlYD5xzKq7aob3NZrNJQzqnSkDlN1vin103SpNsxpEmv2L5ohyaPHSDcPQcI77gBgh8mVOwjsKrObYLpN%2BoTUeN%2F%3C%2Fdiagram%3E%3C%2Fmxfile%3E)
The tables in the image are simplied in terms of columns. In the real databases, customer address table should include more information such as postal code, etc. 
```

***

## Section 2:
You can start this section following *session 4*.

Steps to complete this part of the assignment:
- Open the assignment2.sql file in DB Browser for SQLite:
	- from [Github](./02_activities/assignments/assignment2.sql)
	- or, from your local forked repository  
- Complete each question


### Write SQL

#### COALESCE
1. Our favourite manager wants a detailed long list of products, but is afraid of tables! We tell them, no problem! We can produce a list with all of the appropriate details. 

Using the following syntax you create our super cool and not at all needy manager a list:
```
SELECT 
product_name || ', ' || product_size|| ' (' || product_qty_type || ')'
FROM product
```

But wait! The product table has some bad data (a few NULL values). 
Find the NULLs and then using COALESCE, replace the NULL with a blank for the first column with nulls, and 'unit' for the second column with nulls. 

**HINT**: keep the syntax the same, but edited the correct components with the string. The `||` values concatenate the columns into strings. Edit the appropriate columns -- you're making two edits -- and the NULL rows will be fixed. All the other rows will remain the same.

<div align="center">-</div>

#### Windowed Functions
1. Write a query that selects from the customer_purchases table and numbers each customer’s visits to the farmer’s market (labeling each market date with a different number). Each customer’s first visit is labeled 1, second visit is labeled 2, etc. 

You can either display all rows in the customer_purchases table, with the counter changing on each new market date for each customer, or select only the unique market dates per customer (without purchase details) and number those visits. 

**HINT**: One of these approaches uses ROW_NUMBER() and one uses DENSE_RANK().

2. Reverse the numbering of the query from a part so each customer’s most recent visit is labeled 1, then write another query that uses this one as a subquery (or temp table) and filters the results to only the customer’s most recent visit.

3. Using a COUNT() window function, include a value along with each row of the customer_purchases table that indicates how many different times that customer has purchased that product_id.

<div align="center">-</div>

#### String manipulations
1. Some product names in the product table have descriptions like "Jar" or "Organic". These are separated from the product name with a hyphen. Create a column using SUBSTR (and a couple of other commands) that captures these, but is otherwise NULL. Remove any trailing or leading whitespaces. Don't just use a case statement for each product! 

| product_name               | description |
|----------------------------|-------------|
| Habanero Peppers - Organic | Organic     |

**HINT**: you might need to use INSTR(product_name,'-') to find the hyphens. INSTR will help split the column. 

2. Filter the query to show any product_size value that contain a number with REGEXP. 

<div align="center">-</div>

#### UNION
1. Using a UNION, write a query that displays the market dates with the highest and lowest total sales.

**HINT**: There are a possibly a few ways to do this query, but if you're struggling, try the following: 1) Create a CTE/Temp Table to find sales values grouped dates; 2) Create another CTE/Temp table with a rank windowed function on the previous query to create "best day" and "worst day"; 3) Query the second temp table twice, once for the best day, once for the worst day, with a UNION binding them. 

***

## Section 3:
You can start this section following *session 5*.

Steps to complete this part of the assignment:
- Open the assignment2.sql file in DB Browser for SQLite:
	- from [Github](./02_activities/assignments/assignment2.sql)
	- or, from your local forked repository  
- Complete each question

### Write SQL

#### Cross Join
1. Suppose every vendor in the `vendor_inventory` table had 5 of each of their products to sell to **every** customer on record. How much money would each vendor make per product? Show this by vendor_name and product name, rather than using the IDs.

**HINT**: Be sure you select only relevant columns and rows. Remember, CROSS JOIN will explode your table rows, so CROSS JOIN should likely be a subquery. Think a bit about the row counts: how many distinct vendors, product names are there (x)? How many customers are there (y). Before your final group by you should have the product of those two queries (x\*y). 

<div align="center">-</div>

#### INSERT
1. Create a new table "product_units". This table will contain only products where the `product_qty_type = 'unit'`. It should use all of the columns from the product table, as well as a new column for the `CURRENT_TIMESTAMP`.  Name the timestamp column `snapshot_timestamp`.

2. Using `INSERT`, add a new row to the product_unit table (with an updated timestamp). This can be any product you desire (e.g. add another record for Apple Pie). 

<div align="center">-</div>

#### DELETE 
1. Delete the older record for the whatever product you added.

**HINT**: If you don't specify a WHERE clause, [you are going to have a bad time](https://imgflip.com/i/8iq872).

<div align="center">-</div>

#### UPDATE
1. We want to add the current_quantity to the product_units table. First, add a new column, `current_quantity` to the table using the following syntax.
```
ALTER TABLE product_units
ADD current_quantity INT;
```

Then, using `UPDATE`, change the current_quantity equal to the **last** `quantity` value from the vendor_inventory details. 

**HINT**: This one is pretty hard. First, determine how to get the "last" quantity per product. Second, coalesce null values to 0 (if you don't have null values, figure out how to rearrange your query so you do.) Third, `SET current_quantity = (...your select statement...)`, remembering that WHERE can only accommodate one column. Finally, make sure you have a WHERE statement to update the right row, you'll need to use `product_units.product_id` to refer to the correct row within the product_units table. When you have all of these components, you can run the update statement.
*** 

## Section 4:
You can start this section anytime.

Steps to complete this part of the assignment:
- Read the article
- Write, within this markdown file, <1000 words.

### Ethics

Read: Boykis, V. (2019, October 16). _Neural nets are just people all the way down._ Normcore Tech. <br>
    https://vicki.substack.com/p/neural-nets-are-just-people-all-the

**What are the ethical issues important to this story?**

Consider, for example, concepts of labour, bias, LLM proliferation, moderating content, intersection of technology and society, ect. 


```
When we think of AI tools, we often picture this tool that is highly automated and can do tasks which humans cannot do. 
However, the reality is that human decisions are central to every stage of the development of an AI tool, especially the curation of large data training sets, as described by the article from Vicki Boykis. 
AI tools are not exempted from many potential ethical issues, on the contrary, AIs could potentially amplify existing ethical issues, such as fairness, biases, prejudices, and more. An example I have encountered was that, when an AI tool was asked to make an image of a man and woman, specifically a strong muscular woman, none of the returned images met the requirement as they all showed a muscular man and a slender woman. 
It is hard to explain why this occurs without considering the training dataset behind each tool. If AIs have never “seen” something, it’s hard for them to generate what is asked of them.
It is apparent that human labour and input remain essential for AI development, therefore it is important to clarify the involvement of human efforts, especially at early stages of development. 
To mitigate incidences like this, the selected training data sets need to be very carefully ascertained to actively avoid biases like this. 
It is also as important to educate AI users, which are growing in numbers by the day to understand the capabilities and limitations of the tools at their fingertips so they can be mindful about how they are using the tool and what they are getting out of it. 
```
