# Movies Analysis

1.To get all the tv shows which have 2 or more than 2 seasons 

Use netflix;
select title ,duration,type
FROM netflix_titles
where duration >=2 and type='tv show';

2.To get latest movie released 

select title,type,date_added
FROM netflix_titles
where date_added=(select date_added 
FROM netflix_titles 
order by date_added desc limit 1) and type='movie';

3.To get a list of movies starting  from longest durstion to shortest 

select title,type,duration
from netflix_titles
order by duration desc;

4.To find number of movies where director of movie is not mentioned 
select *
from netflix_titles
where director=''
;

5.To get the list of the movies and tv shows starting with "d"

select title
from netflix_titles
where title like 'd%';


