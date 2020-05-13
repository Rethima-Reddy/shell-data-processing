# shell-data-processing notes
## In power shell
- copy the url (any) as per your specification. 
- In powershell, type the command ```curl "url" ``` the url is the copied url in above step.
- To store this data into a file, we use ```curl "url" -O data.txt ``` where data.txt is the destination file to store data.

## To process the stored text data
- ``` tr ' ' '\12' <data.txt ``` this command transform each '' into '\12' 
- ``` tr ' ' '\12' <data.txt | sort ``` this command will sort the data
- ``` tr ' ' '\12' <data.txt | sort | uniq -c ``` this command will sort the data and will show the count of the unique characters.
- ``` tr ' ' '\12' <data.txt | sort | uniq -c | sort -nr ``` this command will sort the data and shows the most duplicate data to apprear to top.
- ``` tr ' ' '\12' <data.txt | sort | uniq -c | sort -nr > result.txt``` this command will store the data into result.txt file.<br>
Note: The up approw will display the command which we have executed just before it.

## Bash Commands
- ``` ls > filelist.txt``` this will redirect the contents
- ``` ls >> filelist.txt``` (two arrows )this will append the contents
- ``` ls > temp.txt``` saves the contents to new file.
- ``` cat temp.txt``` displays the contents of temp.txt file
- ``` ls``` displays the list of files in that folder.

## The command you used to find the most common words, sorted.
- ```  tr ' ' '\12' <data.txt | sort | uniq -c | sort -nr ``` is the command to find the most common word in the text file.
