## File Match Verifier

It's a work in progress... I will finish it later.

I have been downloading a lot of movies and TV series recently to grow my collection. And one  of the issues I encountered while downloading 10-30 files together using torrent clients was making sure if I have downloaded the movies/TV series that I was supposed to download.

Usual process looked like this:  
* I download 10-20 movies/TV series
* Check the list for which one I downloaded and cross them out so that I don't download the same file again
* Also, it is likely that I might have missed one

It takes time to go through  a long list and find the ones I downloaded. So, i made this script to make life easier.  

Now the process looks like this:

* I download 10-20 movies/TV Series
* I run the script

**So, what exactly does the script do? Good question.**

I keep a list of all the movies I watch and each line looks similar to the following:  
```
1. The Wolf of Wall Street ***** 😂 x3
2. Life of Pi ***** x2
3. The Dictator ***** 🤣 x4

... [continues]
```

Basically, each line structure looks like this:  

`Number` `Name` `Review` `Emoticon` `Times I Have Watched`  

First, the script modifies this data using `data_clear` function by only keeping the names and creating a new `txt` file for processing.
Then, it goes through each line and checks if the movie/tv series is available in a certain directory. If so, it gets rid of that line and updates the text file.

That way I don't have to update it manually, saving me time to work on other important things.  

I am planning to update this code to use for automating the downloading process instead of just verifying file downloads. But I guess that's for another time.