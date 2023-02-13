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


The next unique variation is `grep ...\|... filename`. This command will search the given file for either the string before the `\|` or after. All paragraphs containing either of these strings will be printed in order. This call can be great for searchig a large .txt file for two important key words. This variation of `grep` was found on the website "thegeekstuff." [Click Here](https://www.thegeekstuff.com/2011/10/grep-or-and-not-operators/)

```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep 'judiciary\|Lucayans' ./written_2/travel_guides/Berlitz2/Bahamas-History.txt
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
Since independence the Bahamas has kept British systems of judiciary and government yet has moved closer economically to its near neighbor, the US. The Bahamian Government has deliberately pursued tourism as the major industry of the Bahamian commonwealth and is happy to welcome many millions of visitors to its shores. The growth in cruise traffic has been particularly strong. The other islands, called the Family Islands by the government but generally referred to as the Out Islands by the tourist trade, have not shared this huge growth in numbers of visitors. Together they offer tourists almost any form of vacation experience, from the bustle of the busy city to the silence of the desert island.
```
* As seen above, three paragraphs were returned from this `grep` call. In the first and second paragraph, the word "Lucayans" can be seen. In the third paragraph, the word "judiciary" is located in there. 

```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep 'California\|Lucayans' ./written_2/travel_guides/Berlitz2/Bahamas-History.txt
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

* This code returned two paragraphs. The only thing changed was the first word, from "judiciary" to "California". Now, the two paragraphs returned are the two paragraphs containing the word "Lucayans." Even though the first word, "California", was not found, the `grep` call still searched for the others. This is because the `\|` stand for "or", and if one of the two strings do not exist in the file, the call will search for the other string. 

Another unqiue instance of `grep` is `grep -i`. When normally calling `grep` in the terminal, the search for the given string is case sensitive, so even a simple mistake of wrong capitalization can lead to a mistake. By adding the `-i`, the grep call is now not case sensitive. This call is beneficial for searching for a key word that may by at the start of the sentnece, middle, or all capitalized in some instances within the file. Also, `-i` is actually short for `--ignore-case`. So, using either of these after the `grep` call with both result in a string search that is not case sensitive. This instance of `grep` came from asking ChatGPT for unique and alternative instances of `grep`.

```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep -iRl "LUCAYANS"
./written_2/travel_guides/berlitz2/Bahamas-History.txt
```

* In this first example, `-i` is actually called with one of the other unique commands talked about earlier, `-Rl`. By combining the two commands, the search is now looking for "LUCAYANS" without case sensitivity and returning the path to the file holding any variation of the string, with capitals or without. 

```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep -i "LUCayaNS" written_2/travel_guides/berlitz2/Bahamas-History.txt
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
The Spaniards never bothered to settle in the Bahamas, but the number of shipwrecks attest that their galleons frequently passed through the archipelago en route to and from the Caribbean, Florida, Bermuda, and their home ports. On Eleuthera the explorers dug a fresh-water well — at a spot now known as “Spanish Wells” — which was used to replenish the supplies of water on their ships before they began the long journey back to Europe with their cargoes of South American gold. As for the Lucayans, within 25 years all of them, perhaps some 30,000 people, were removed from the Bahamas to work — and die — in Spanish gold mines and on farms and pearl fisheries on Hispaniola (Haiti), Cuba, and elsewhere in the Caribbean.
```

* In this specific call, I input the string "LUCayaNS." Normally, the `grep` call would not have found this string due to the peculiar capitalization. However, the `-i` make the search case insensitive. Also, a direct path to Bahamas-History.txt is provided, so this call will search the strings contained within this .txt file. 

A fourth unique call is `grep -c` or `grep --count`. Both of these calls do the same thing which is to count the number of matches with the string, rather than the actual lines. This is especially helpful for large .txt files. Earlier in this report, some of the calls returned huge paragraphs taken from the .txt file, containing the specific word we were searching for. Instead of searching through the paragraphs and having the paragraphs take up huge portions of the terminal and crowd the code, this call will simply tell the numebr of occurences that this string is in the file.  

```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep -c "Lucayans" written_2/travel_guides/berlitz2/Bahamas-History.txt                                           
2
```

* This is a very similar command to the ones shown above. The same string, "Lucayans", is being searched for in the same .txt file, Bahamas-History.txt. However, instead of seeing the two parargaphs containing this string, now we only see the number two returned from the terminal, saying there are two instances of this string wihtin the file.

```
davidmontoto@Davids-MacBook-Air-2 skill-demo1-data % grep -c "the" written_2/travel_guides/berlitz2/Bahamas-History.txt
30
```

* This version of `grep` is exceptional when one is searching for a word that may be prominant throughout the .txt file. For example, the word "the" is more than likely used many times in the .txt file. Instead of having thirty or so paragraphs from the .txt file be returned in the terminal, the number 30 is returned which is much cleaner and still shows how many times the string is used. 


