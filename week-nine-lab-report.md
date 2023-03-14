# Lab Report 3
## By David Montoto

### Alternative and Unique Ways of Utilizing `find`

The first interesting variation of `find` is `find . -type d`. This variation is used to find all directories within the gicurrentven path. Using `-type d` is why it is only searching for directories in the given path and nothing else.

```
davidmontoto@Davids-Air-2 written_2 % find . -type d
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Berk
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Rybczynski
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Castro
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```

* As you can see, I am already in the written_2 directory. So, for the path, I simply use `.` so the terminal knows that this is the path I want it to search through instead of specifying something else. 

```
davidmontoto@Davids-Air-2 non-fiction % find . -type d

.
./OUP
./OUP/Berk
./OUP/Abernathy
./OUP/Rybczynski
./OUP/Kauffman
./OUP/Fletcher
./OUP/Castro
```

* Here, I am in the `non-fiction` directory contained within the `written_2` directory. So when I call the same thing into the terminal, we see some of the directories shown in the first call but not all because now we are in a deeper directory.

The next version of `find` is `find [path] -size [size] [unit]`. This iteration of find is searching and macthing only with directories that fit the size constraint. So this call is great for looking for files that are bigger or less than the desired size. One can use either a `-` or `+` to specifiy greater than or less than the size constraint. This unique variation was found by asking ChatGPT for a unique instance of `find`. 

```
davidmontoto@Davids-Air-2 non-fiction % find . -size -1k
.
./OUP
./OUP/Berk
./OUP/Abernathy
./OUP/Rybczynski
./OUP/Kauffman
./OUP/Fletcher
./OUP/Castro
```

* In this example, I use `-1k` which means I am looking for subdirectories in the current path that are less than one kilobyte.

```
davidmontoto@Davids-Air-2 non-fiction % find . -size +10M
```

* In this example, you can see that nothing was returned when I was looking for directories or files that are larger than ten megabytes. If working with size contraints by a company, this is wonderful for ensuring no files are breaking a size constraint. 

