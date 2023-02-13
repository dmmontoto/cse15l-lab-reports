# Lab Report 3
## By David Montoto

### Alternative and Unique Ways of Utilizing `grep`

The first interesting variation of `grep` is `grep -Rl`. This variation is used to search for a pattern in a directory tree and to print only the names of the files that contain the pattern, not the actual lines that match the pattern. The -R option specifies a recursive search, and the -l option specifies to print only the file names, not the matching lines. This call shows the path of the file containing the specific string that was searched. This variation was found after asking ChatGPT for a unique and interesting variation of `grep`.

```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep -Rl "Lucayans"
./written_2/travel_guides/berlitz2/Bahamas-History.txt
```
* In the code block, you can see that the only thing printed in the terminal is the path for the .txt file containing the word "Lucayans."
```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep -Rl "California"
./.git/index
./written_2/non-fiction/OUP/Berk/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt
./written_2/non-fiction/OUP/Abernathy/ch15.txt
./written_2/non-fiction/OUP/Rybczynski/ch2.txt
./written_2/non-fiction/OUP/Rybczynski/ch1.txt
./written_2/non-fiction/OUP/Kauffman/ch1.txt
./written_2/non-fiction/OUP/Kauffman/ch9.txt
./written_2/non-fiction/OUP/Fletcher/ch9.txt
./written_2/non-fiction/OUP/Castro/chR.txt
./written_2/non-fiction/OUP/Castro/chP.txt
./written_2/non-fiction/OUP/Castro/chQ.txt
./written_2/non-fiction/OUP/Castro/chB.txt
./written_2/non-fiction/OUP/Castro/chC.txt
./written_2/non-fiction/OUP/Castro/chA.txt
./written_2/non-fiction/OUP/Castro/chV.txt
./written_2/non-fiction/OUP/Castro/chW.txt
./written_2/non-fiction/OUP/Castro/chM.txt
./written_2/non-fiction/OUP/Castro/chL.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/HistoryLasVegas.txt
./written_2/travel_guides/berlitz1/HandRLosAngeles.txt
./written_2/travel_guides/berlitz1/WhereToMallorca.txt
./written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
./written_2/travel_guides/berlitz1/WhatToLasVegas.txt
./written_2/travel_guides/berlitz1/WhatToLosAngeles.txt
./written_2/travel_guides/berlitz2/California-WhereToGo.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/California-History.txt
./written_2/travel_guides/berlitz2/California-WhatToDo.txt
```
* In the code block, multiple different paths were returned, each going to a different file. This is because there are a multiple .txt files in written_2 that contain the work "California."


The next 



@Test
public void testReverseInPlace2() {
  int[] input1 = {1, 2, 3, 4, 5};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{5, 4, 3, 2, 1}, input1);
}

@Test
public void testReversed1() {
  int[] input1 = {1, 2, 3, 4};
  assertArrayEquals(new int[]{4, 3, 2, 1}. ArrayExamples.reversed(input1));
}
```

