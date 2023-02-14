# Lab Report 3

I'll be using the **grep** command :D.

All my examples came from https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix

## grep -r "string" file-name/directory
**EX1)**

Input:
`
andyho@Andys-MacBook-Air Abernathy % grep -r "In the late 1940s"`

Output:
`./ch1.txt:In the late 1940s, Bond Stores, the largest men’s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.`

Explanation:
This command takes in the string pattern "In the late 1940s". It then recursively searches in the current directory (Abernathy) and its subdirectories for exact matches and outputs the lines that contain the match along with the file name. This is useful for looking for specific data inside big data files. 

**EX2)** 

Input: 
`andyho@Andys-MacBook-Air written_2 % grep -r "no matching string"`

Output:
No output :(

Explanation:
This command takes in the string pattern "no matching string". It searches for a line with the matching string, but it does not find any. This is useful for checking if specific patterns exist in a data file.

## grep -c "string" file-name

**EX1)**

Input: 
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Bahamas" Bahamas-History.txt`

Output:
`23`

Explanation:
This command takes in a string pattern "Bahamas" and returns the number of lines that contain that string inside Bahams-History.txt. This command is useful for checking if the string pattern is a common occurance in a text file.

**EX2)**

Input:
`andyho@Andys-MacBook-Air berlitz2 % grep -c "Not Bahamas" Bahamas-History.txt`

Output:
`0`

Explanation:
Takes in the string "Not Bahamas" and counts the number of lines that pattern appears. In this case it's zero, because no line in that file contains it. This is useful for confirming if there is no sentence/word that appears in the text file.

## grep -v "string" file-name

**EX1)**

Input:
`

