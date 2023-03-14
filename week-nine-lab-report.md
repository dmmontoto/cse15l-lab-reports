# Lab Report 5
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

The next unique instance of `find` is find `[path] -name [filename_pattern]`. This call is creat for searching for patterns in names or files and subdirectories that fit various criteria. This instance was found by asking ChatGPT for a unique way to find files using the `find` in terminal. 

```
davidmontoto@Davids-Air-2 non-fiction % find . -name "
????"
./OUP/Berk
```

* Here, I use `????` after the `-name`, which essentially tells the temrinal that I need to find any files or directories that only have four letters in the name. Hence, this is why the only thing returned was `./OUP/Berk`.

```
davidmontoto@Davids-Air-2 non-fiction % find . -name "*.txt"

./OUP/Berk/ch2.txt
./OUP/Berk/ch1.txt
./OUP/Berk/CH4.txt
./OUP/Berk/ch7.txt
./OUP/Abernathy/ch2.txt
./OUP/Abernathy/ch3.txt
./OUP/Abernathy/ch1.txt
./OUP/Abernathy/ch7.txt
./OUP/Abernathy/ch6.txt
./OUP/Abernathy/ch8.txt
./OUP/Abernathy/ch9.txt
./OUP/Abernathy/ch15.txt
./OUP/Abernathy/ch14.txt
./OUP/Rybczynski/ch2.txt
./OUP/Rybczynski/ch3.txt
./OUP/Rybczynski/ch1.txt
./OUP/Kauffman/ch3.txt
./OUP/Kauffman/ch1.txt
./OUP/Kauffman/ch4.txt
./OUP/Kauffman/ch5.txt
./OUP/Kauffman/ch7.txt
./OUP/Kauffman/ch6.txt
./OUP/Kauffman/ch8.txt
./OUP/Kauffman/ch9.txt
./OUP/Kauffman/ch10.txt
./OUP/Fletcher/ch2.txt
./OUP/Fletcher/ch1.txt
./OUP/Fletcher/ch5.txt
./OUP/Fletcher/ch6.txt
./OUP/Fletcher/ch9.txt
./OUP/Fletcher/ch10.txt
./OUP/Castro/chR.txt
./OUP/Castro/chP.txt
./OUP/Castro/chQ.txt
./OUP/Castro/chB.txt
./OUP/Castro/chC.txt
./OUP/Castro/chA.txt
./OUP/Castro/chV.txt
./OUP/Castro/chW.txt
./OUP/Castro/chM.txt
./OUP/Castro/chZ.txt
./OUP/Castro/chL.txt
./OUP/Castro/chN.txt
./OUP/Castro/chY.txt
./OUP/Castro/chO.txt
```

* Here, I wanted to find all `.txt` files contained in the current directory. By using `*.txt`, I was able to achieve that goal.

The last unique iteration of `find` that I found was `find [path] -fstype [filesystem_type]
`. This call is great for checking when was the last time that you modified a file. It can also be used to check if you are working with the right file by seeing if it was editied recently or not. I also asked ChatGPT to find this last unique instance of `find`. 

```
davidmontoto@Davids-Air-2 non-fiction % find . -mtime -30
.
./ch1.txt
./ch7.txt
```

* Before calling this, I made some edits to the two files shown above. When calling this in terminal, it searched the current directory for all files that have been modified in the past thirty days, such as these two. 

```
davidmontoto@Davids-Air-2 non-fiction % find . -mtime +30 
./OUP
./OUP/Berk
./OUP/Berk/ch2.txt
./OUP/Berk/ch1.txt
./OUP/Berk/CH4.txt
./OUP/Berk/ch7.txt
./OUP/Abernathy
./OUP/Abernathy/ch2.txt
./OUP/Abernathy/ch3.txt
./OUP/Abernathy/ch1.txt
./OUP/Abernathy/ch7.txt
./OUP/Abernathy/ch6.txt
./OUP/Abernathy/ch8.txt
./OUP/Abernathy/ch9.txt
./OUP/Abernathy/ch15.txt
./OUP/Abernathy/ch14.txt
./OUP/Rybczynski
./OUP/Rybczynski/ch2.txt
./OUP/Rybczynski/ch3.txt
./OUP/Rybczynski/ch1.txt
./OUP/Kauffman
./OUP/Kauffman/ch3.txt
./OUP/Kauffman/ch1.txt
./OUP/Kauffman/ch4.txt
./OUP/Kauffman/ch5.txt
./OUP/Kauffman/ch7.txt
./OUP/Kauffman/ch6.txt
./OUP/Kauffman/ch8.txt
./OUP/Kauffman/ch9.txt
./OUP/Kauffman/ch10.txt
./OUP/Fletcher
./OUP/Fletcher/ch2.txt
./OUP/Fletcher/ch1.txt
./OUP/Fletcher/ch5.txt
./OUP/Fletcher/ch6.txt
./OUP/Fletcher/ch9.txt
./OUP/Fletcher/ch10.txt
./OUP/Castro
./OUP/Castro/chR.txt
./OUP/Castro/chP.txt
./OUP/Castro/chQ.txt
./OUP/Castro/chB.txt
./OUP/Castro/chC.txt
./OUP/Castro/chA.txt
./OUP/Castro/chV.txt
./OUP/Castro/chW.txt
./OUP/Castro/chM.txt
./OUP/Castro/chZ.txt
./OUP/Castro/chL.txt
./OUP/Castro/chN.txt
./OUP/Castro/chY.txt
./OUP/Castro/chO.txt
```

* For this call, you can see that many files and directories showed up. For this call, I used a plus sign instead of a minus, asking to find the files modified anytime past the most recent thirty days, showing all these. 
