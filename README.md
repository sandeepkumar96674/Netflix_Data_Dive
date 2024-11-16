## Project Title : Netflix Data Analysis

## Get the Dataset from [here](https://drive.google.com/file/d/1xBNNC_0mHvPj_dY1DcKfKdnRzUeLpg7F/view?usp=sharing) 

### About the Dataset:
![image](https://github.com/user-attachments/assets/7690ea3e-c133-4ade-a033-11fc25fcf919)

### Download the Microsoft SQL Server Management Tool here [SQl Server](https://www.microsoft.com/en-in/sql-server/sql-server-downloads) and [MSSM](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16&redirectedfrom=MSDN)

### The Data is Stored in the Table named "Netflix".

### Question solved by the Queries are following:

##### Q1. Count the Number of Movie and TV Shows in type column
```
select count(type) as TV from netflix where type ='TV Show';
select count(type) as movies from netflix where type ='Movie';
 
```

##### Q2. Count of Shows released in each Year
```
select count(title),release_year from netflix group by release_year order by release_year asc;

```

##### Q3. Distinct Type of Shows 
```
select distinct type from netflix;
```

##### Q4. Top-5 Countries with most released shows (Movies/ TV Shows)
```
select country,count(country) as show_count from netflix where country is not null group by country order by show_count desc limit 5;
```
#### Q5. Shows with Director name who has directed show with 5 Seasons
```
select title,director from netflix where duration = '5 Seasons';
```
#### Q6. Shows with it's id who have directors (Director Column should not null)
```
select show_id,title from netflix where director is not null;
```
#### Q7. Shows with the genre "Documentaries"
```
select title,release_year,listed_in from netflix where listed_in = 'Documentaries';
```

#### Q8. Show/Movies directed by "Toshiya Shinohara"

```
select title from netflix where director = 'Toshiya Shinohara';
```

#### You can also get the Insight and Understanding of Data by using the Above Queries.

### Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
```
https://github.com/sandeepkumar96674/Netflix_Data_Analysis.git
```
#### For more please connect with me on [LinkedIn](https://www.linkedin.com/in/the-sandeep-kumar)
