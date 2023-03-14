# Lab Report 5

In this lab report I will be visiting lab report 3 but be using the **find** command.

All my find commands came from [linuxize](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/)

## find "directory path" type "file type"

1. Find file type directories
Input: `andyho@Andys-MacBook-Air written_2 % find . -type d`

Output: `.
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
./travel_guides/berlitz2`

This command finds all the direcotries in the path given. It is pretty useful for seperating the directories from all the other files in the current path. 

2. Find file type files
Input: `andyho@Andys-MacBook-Air written_2 % find non-fiction/OUP/Abernathy -type f`

Output: `non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Abernathy/ch14.txt`

This command found all the txt files inside non-fiction/OUP/Abernathy. It's useful for just only finding txt files inside a directory.

## find "directory path" -size "(+/-)(size type)"

1.
Input: `andyho@Andys-MacBook-Air written_2 % find non-fiction/OUP/Abernathy -size -40k`

Output: `non-fiction/OUP/Abernathy
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Abernathy/ch14.txt`

This command found all the files with a size less than 40 kilobytes inside Abernathy. It's useful for finding files under a certain size.

2.
Input: `andyho@Andys-MacBook-Air written_2 % find non-fiction/OUP/Abernathy -size +50k`

Output: `non-fiction/OUP/Abernathy/ch8.txt`

This command found all the files with a size more than 50 kilobytes inside Abernathy. It's useful for bigger files inside a directory.

## find "directory path" -name "(extension name)"

1.
Input: `andyho@Andys-MacBook-Air written_2 % find non-fiction/OUP/Berk -name '*.txt'`

Output: `non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Berk/CH4.txt
non-fiction/OUP/Berk/ch7.txt`

This command finds the all the files inside Berk that end with "txt". It's useful for find certain types of files like text files or even java files.

2. 
Input: `andyho@Andys-MacBook-Air written_2 % find travel_guides -name '*History.txt'`

Output: `travel_guides/berlitz2/Portugal-History.txt
travel_guides/berlitz2/Costa-History.txt
travel_guides/berlitz2/Barcelona-History.txt
travel_guides/berlitz2/Berlin-History.txt
travel_guides/berlitz2/Bali-History.txt
travel_guides/berlitz2/Athens-History.txt
travel_guides/berlitz2/California-History.txt
travel_guides/berlitz2/Vallarta-History.txt
travel_guides/berlitz2/Cancun-History.txt
travel_guides/berlitz2/CostaBlanca-History.txt
travel_guides/berlitz2/NewOrleans-History.txt
travel_guides/berlitz2/PuertoRico-History.txt
travel_guides/berlitz2/Nepal-History.txt
travel_guides/berlitz2/China-History.txt
travel_guides/berlitz2/Canada-History.txt
travel_guides/berlitz2/Crete-History.txt
travel_guides/berlitz2/Amsterdam-History.txt
travel_guides/berlitz2/Beijing-History.txt
travel_guides/berlitz2/CanaryIslands-History.txt
travel_guides/berlitz2/Algarve-History.txt
travel_guides/berlitz2/Poland-History.txt
travel_guides/berlitz2/Budapest-History.txt
travel_guides/berlitz2/Cuba-History.txt
travel_guides/berlitz2/Bahamas-History.txt`

This command finds all of the travel guides that end with history. This was useful for finding only the files that are the history of countries. 

## find "directory path" -name 'extension' -delete

1.
Input: `andyho@Andys-MacBook-Air written_2 % find non-fiction/OUP/Abernathy -name '*.txt' -delete`

Output: Nothing, but after doing `andyho@Andys-MacBook-Air written_2 % find non-fiction/OUP/Abernathy`
And that outputs: `non-fiction/OUP/Abernathy`

This command deleted all the files inside Abernathy that ended with '.txt', in this case it was all the files. It's useful for deleting certain types of files.

2. 
Input: `find travel_guides/berlitz2 find travel_guides/berlitz2 -name '*History.txt' -delete`
Output: (`After doing andyho@Andys-MacBook-Air written_2 % find travel_guides/berlitz2`):
`travel_guides/berlitz2
travel_guides/berlitz2/Berlin-WhereToGo.txt
travel_guides/berlitz2/Amsterdam-WhereToGo.txt
travel_guides/berlitz2/Costa-WhereToGo.txt
travel_guides/berlitz2/Amsterdam-WhatToDo.txt
travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
travel_guides/berlitz2/Portugal-WhereToGo.txt
travel_guides/berlitz2/Boston-WhereToGo.txt
travel_guides/berlitz2/Poland-WhatToDo.txt
travel_guides/berlitz2/California-WhereToGo.txt
travel_guides/berlitz2/Cuba-WhatToDo.txt
travel_guides/berlitz2/Bahamas-WhereToGo.txt
travel_guides/berlitz2/Cancun-WhatToDo.txt
travel_guides/berlitz2/Crete-WhereToGo.txt
travel_guides/berlitz2/Berlin-WhatToDo.txt
travel_guides/berlitz2/Canada-WhereToGo.txt
travel_guides/berlitz2/Bali-WhereToGo.txt
travel_guides/berlitz2/Budapest-WhereoGo.txt
travel_guides/berlitz2/Barcelona-WhereToGo.txt
travel_guides/berlitz2/Athens-WhereToGo.txt
travel_guides/berlitz2/Paris-WhereToGo.txt
travel_guides/berlitz2/China-WhereToGo.txt
travel_guides/berlitz2/Bermuda-WhatToDo.txt
travel_guides/berlitz2/Budapest-WhatToDo.txt
travel_guides/berlitz2/PuertoRico-WhatToDo.txt
travel_guides/berlitz2/Vallarta-WhatToDo.txt
travel_guides/berlitz2/Bali-WhatToDo.txt
travel_guides/berlitz2/CstaBlanca-WhereToGo.txt
travel_guides/berlitz2/Algarve-Intro.txt
travel_guides/berlitz2/Portugal-WhatToDo.txt
travel_guides/berlitz2/Bahamas-Intro.txt
travel_guides/berlitz2/Bahamas-WhatToDo.txt
travel_guides/berlitz2/Barcelona-WhatToDo.txt
travel_guides/berlitz2/Algarve-WhatToDo.txt
travel_guides/berlitz2/PuertoRico-WhereToGo.txt
travel_guides/berlitz2/Cuba-WhereToGo.txt
travel_guides/berlitz2/Costa-WhatToDo.txt
travel_guides/berlitz2/Nepal-WhereToGo.txt
travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
travel_guides/berlitz2/Bermuda-history.txt
travel_guides/berlitz2/Amsterdam-Intro.txt
travel_guides/berlitz2/Crete-WhatToDo.txt
travel_guides/berlitz2/Algarve-WhereToGo.txt
travel_guides/berlitz2/Athens-Intro.txt
travel_guides/berlitz2/Beijing-WhereToGo.txt
travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
travel_guides/berlitz2/California-WhatToDo.txt
travel_guides/berlitz2/China-WhatToDo.txt
travel_guides/berlitz2/Athens-WhatToDo.txt
travel_guides/berlitz2/Nepal-WhatToDo.txt
travel_guides/berlitz2/Bermuda-WhereToGo.txt
travel_guides/berlitz2/Paris-WhatToDo.txt
travel_guides/berlitz2/Vallarta-WhereToGo.txt
travel_guides/berlitz2/Beijing-WhatToDo.txt
travel_guides/berlitz2/Cancun-WhereToGo.txt`

This command deleted all the files inside berlitz2 that ended with "History.txt". It's useful for deleting certain types of files. 
