### File Structure 
1.Created **hello** directory by using command ***mkdir hello***

2.changed to **hello** directory using command ***cd hello***

3.create two directories in hello named **five** and **one** using comands ***mkdir five*** and ***mkdir one***

4.changed to **five** directory using command ***cd five***

5.created one directory named **six** using command ***mkdir six***

6.changed to **six** directory using command ***cd six***

7.Created one text file named **c** using command ***touch c.txt*** and created one directory named **seven** using command ***mkdir seven***

8.change to **seven** directory using command ***cd seven***

9.created a log file named **error** using command ***touch error.log***

10.changed to **one** directory using commands ***cd ..*** and ***cd one***

11.created two text files named **a** and **b** using commands ***touch a.txt*** , ***touch b.txt*** and one directory named **two** using command ***mkdir two***

12.change to **two** directory using command ***cd two***

13.created one text file named **d** using command ***touch d.txt*** and one directory named **three** using command ***mkdir three***

14.changed to **three** directory using command ***cd three***

15.created one text file named **e** usign command ***touch e.txt*** and one directory named **four** using command ***mkdir four***

16.switched to **four** directory using command ***cd four***

17.created a log file named **access** using command ***touch access.log***



## Download and Text Processing

1. Downloaded the book **Harry Potter and the Goblet of Fire** using command  
   ***wget https://www.gutenberg.org/files/210/210-0.txt -O goblet.txt***

2. Printed the first three lines of the book using command  
   ***head -n 3 goblet.txt***

3. Printed the last ten lines of the book using command  
   ***tail -n 10 goblet.txt***

4. Counted occurrences of **Harry** using command  
   ***grep -oiw "harry" goblet.txt | wc -l***

5. Counted occurrences of **Ron** using command  
   ***grep -oiw "ron" goblet.txt | wc -l***

6. Counted occurrences of **Hermione** using command  
   ***grep -oiw "hermione" goblet.txt | wc -l***

7. Counted occurrences of **Dumbledore** using command  
   ***grep -oiw "dumbledore" goblet.txt | wc -l***

8. Printed lines from 100 through 200 in the book using command  
   ***sed -n '100,200p' goblet.txt***

9. Counted total unique words in the book using command  
   ***tr -cs '[:alnum:]' '\n' < goblet.txt | tr 'A-Z' 'a-z' | sort | uniq | wc -l***



##  Processes and Ports

1. Listed browser process IDs using command  
    ***pgrep firefox***

2. Stopped the browser application using command  
    ***pkill firefox***

3. Checked the top CPU consuming processes using command  
    ***top***  
    Then pressed ***P*** to sort by CPU usage.

4. Checked the top memory consuming processes using command  
    ***top***  
    Then pressed ***M*** to sort by memory usage.


5. Started a Python HTTP server on port 8000 using command  
    ***python3 -m http.server 8000***

6. Displayed the process and PID listening on port **8000** using command  
***sudo netstat -tulnp | grep :8000*** 
    and terminating it using  
    ***kill <PID>***

7. Started a Python HTTP server on port 90 using command  
    ***sudo python3 -m http.server 90***

8. Displayed all active TCP / UDP connections using command  
    ***ss -tulnp***

9. Found the PID of the process listening on port 5432 using command  
    ***sudo ss -tulnp | grep :5432***


##  Managing Software

1. Updated package list using command  
    ***sudo apt update***

2. Installed **htop**, **vim**, and **nginx** using command  
    ***sudo apt install htop vim nginx***

3. Uninstalled nginx using command  
    ***sudo apt remove nginx***



##  Networking and System

1. Displayed local IP address using command  
    ***ip addr show***

2. Found IP address of google.com using command  
    ***nslookup google.com***

3. Checked internet connectivity using command  
    ***ping 8.8.8.8***

4. Found the location of **node** command using command  
    ***which node***

5. Found the location of **code** command using command  
    ***which code***


