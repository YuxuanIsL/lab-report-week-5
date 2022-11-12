# Lab report 3 for week 5

## `find` command-line options

***

```
$ find ./technical/911report -name chapter-1.txt
```

```
./technical/911report/chapter-1.txt
```

This command line option searches files that match the given name in your specified directory. It is useful when you want to find the specific file.

***

```
$ find ./technical/911report *.txt
```
```
./technical/911report
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```

This command line option searches files in your specified directory with file names end with '.txt' It is useful when you sometimes want to see certain types of files (which typically end with category names) in a path.

***

```
$ find ./technical/911report -name chapter-2.txt -exec rm -i {} \;
```
```
remove ./technical/911report/chapter-2.txt?
```

If you then type `Y/y`, it will delete the file `chapter-2.txt`.

This command line option helps to search in the specified directory and find the file then delete it for you. It is useful when you want to remove a file from terminal.

***

## `less` command-line options

***

```
$ less -N ./technical/911report/chapter-2.txt
```

```
      1 
      2     
      3         
      4             THE FOUNDATION OF THE NEW TERRORISM
      5             A DECLARATION OF WAR
      6             In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egyptian
      7                 physician, Ayman al Zawahiri, arranged from their Afghan headquarters for an Arabic
      8                 newspaper in London to publish what they termed a fatwa issued in the name of a
      9                 "World Islamic Front." A fatwa is normally an interpretation of Islamic law by a
     10                 respected Islamic authority, but neither Bin Ladin, Zawahiri, nor the three others
     11                 who signed this statement were scholars of Islamic law. Claiming that America had
     12                 declared war against God and his messenger, they called for the murder of any
     13                 American, anywhere on earth, as the "individual duty for every Muslim who can do it
     14                 in any country in which it is possible to do it."
     15             
     16             Three months later, when interviewed in Afghanistan by ABC-TV, Bin Ladin enlarged on
     17                 these themes.
     18             
     19             He claimed it was more important for Muslims to kill Americans than to kill other
     20                 infidels." It is far better for anyone to kill a single American soldier than to
     21                 squander his efforts on other activities," he said. Asked whether he approved of
     22                 terrorism and of attacks on civilians, he replied:"We believe that the worst thieves
     23                 in the world today and the worst terrorists are the Americans. Nothing could stop
     24                 you except perhaps retaliation in kind. We do not have to differentiate between
     25                 military or civilian. As far as we are concerned, they are all targets." Note:
```
This command line option gives information in a screenly-visible manner with number of lines in front of each line. It is useful when you want to see not only the contents but also the line numbers of a file.
***
```
$ less -s ./technical/911report chapter-6.txt
```
```
            FROM THREAT TO THREAT
            In chapters 3 and 4 we described how the U.S. government adjusted its existing
                agencies and capacities to address the emerging threat from Usama Bin Ladin and his
                associates. After the August 1998 bombings of the American embassies in Kenya and
                Tanzania, President Bill Clinton and his chief aides explored ways of getting Bin
                Ladin expelled from Afghanistan or possibly capturing or even killing him. Although
                disruption efforts around the world had achieved some successes, the core of Bin
                Ladin's organization remained intact. President Clinton was deeply concerned about
                Bin Ladin. He and his national security advisor, Samuel "Sandy" Berger, ensured they
                had a special daily pipeline of reports feeding them the latest updates on Bin
                Ladin's reported location.
            
            In public, President Clinton spoke repeatedly about the threat of terrorism,
                referring to terrorist training camps but saying little about Bin Ladin and nothing
                about al Qaeda. He explained to us that this was deliberate-intended to avoid
                enhancing Bin Ladin's stature by giving him unnecessary publicity. His speeches
                focused especially on the danger of nonstate actors and of chemical and biological
                    weapons.
            
            As the millennium approached, the most publicized worries were not about terrorism
                but about computer breakdowns-the Y2K scare. Some government officials were
                concerned that terrorists would take advantage of such breakdowns.
```
This command line option squeezes multiple blank lines from a text file into one blank line. Removing multiple blank lines allows less to show more content in each screenful of the file.
***
```
$ less ./technical/911report/chapter-6.txt ./technical/911report/chapter-7.txt
```
```
            FROM THREAT TO THREAT
            In chapters 3 and 4 we described how the U.S. government adjusted its existing
                agencies and capacities to address the emerging threat from Usama Bin Ladin and his
                associates. After the August 1998 bombings of the American embassies in Kenya and
                Tanzania, President Bill Clinton and his chief aides explored ways of getting Bin
                Ladin expelled from Afghanistan or possibly capturing or even killing him. Although
                disruption efforts around the world had achieved some successes, the core of Bin
                Ladin's organization remained intact. President Clinton was deeply concerned about
                Bin Ladin. He and his national security advisor, Samuel "Sandy" Berger, ensured they
                had a special daily pipeline of reports feeding them the latest updates on Bin
                Ladin's reported location.
            
            In public, President Clinton spoke repeatedly about the threat of terrorism,
                referring to terrorist training camps but saying little about Bin Ladin and nothing
                about al Qaeda. He explained to us that this was deliberate-intended to avoid
                enhancing Bin Ladin's stature by giving him unnecessary publicity. His speeches
                focused especially on the danger of nonstate actors and of chemical and biological
                    weapons.
            
            As the millennium approached, the most publicized worries were not about terrorism
                but about computer breakdowns-the Y2K scare. Some government officials were
                concerned that terrorists would take advantage of such breakdowns.
./technical/911report/chapter-6.txt (file 1 of 2)
```
This allows open multiple files simultaneously using less without losing the current position in the files. To open multiple files, specify file names one after another. 

Move to the next file by pressing the `: key` followed by `n`.

Return to the previous file by pressing `:` and `p`.

***
```
$ less -X ./technical/911report/chapter-6.txt
```
```
            FROM THREAT TO THREAT
            In chapters 3 and 4 we described how the U.S. government adjusted its existing
                agencies and capacities to address the emerging threat from Usama Bin Ladin and his
                associates. After the August 1998 bombings of the American embassies in Kenya and
                Tanzania, President Bill Clinton and his chief aides explored ways of getting Bin
                Ladin expelled from Afghanistan or possibly capturing or even killing him. Although
                disruption efforts around the world had achieved some successes, the core of Bin
                Ladin's organization remained intact. President Clinton was deeply concerned about
                Bin Ladin. He and his national security advisor, Samuel "Sandy" Berger, ensured they
                had a special daily pipeline of reports feeding them the latest updates on Bin
                Ladin's reported location.
            
            In public, President Clinton spoke repeatedly about the threat of terrorism,
                referring to terrorist training camps but saying little about Bin Ladin and nothing
                about al Qaeda. He explained to us that this was deliberate-intended to avoid
                enhancing Bin Ladin's stature by giving him unnecessary publicity. His speeches
                focused especially on the danger of nonstate actors and of chemical and biological
                    weapons.
            
            As the millennium approached, the most publicized worries were not about terrorism
                but about computer breakdowns-the Y2K scare. Some government officials were
                concerned that terrorists would take advantage of such breakdowns.
```
After quitting less, the terminal window clears, removing the file output. To leave the file contents in the terminal after quitting, specify the -X option.

The shown output will be kept on the terminal display screen after `q`

## `grep` command-line options
***
```
$ grep -i "WHat" ./technical/911report/chapter-7.txt
```
```
            To understand what Hazmi and Mihdhar did in their first weeks in the United States,
                somewhat suspect. (He likewise denied knowing Omar al Bayoumi-a man from San Diego
                heard Hazmi and Mihdhar speaking in what he recognized to be Gulf Arabic and struck
                claimed not to remember any specifics of what they discussed. He described Hazmi as
            Saudi authorities interviewed the relatives of these men and have briefed us on what
                recruit would fill out an application with standard questions, such as, What brought
                you to Afghanistan? How did you travel here? How did you hear about us? What
                attracted you to the cause? What is your educational background? Where have you
            We have found no evidence that Iran or Hezbollah was aware of the planning for what
                Corridor, but his instructor declined a second request because of what he considered
                money, could not speak English, and could not adequately explain what he intended to
```
The -i option enables to search for a string case insensitively in the given file. It is useful when you want to look up lines in a file that contains certain words.
***
```
$ grep -c "what" ./technical/911report/chapter-7.txt
```
```
8
```
This helps to find the number of lines that matches the given string/pattern. 
***
```
$ grep -n "what" ./technical/911report/chapter-7.txt
```
```
65:            To understand what Hazmi and Mihdhar did in their first weeks in the United States,
91:                somewhat suspect. (He likewise denied knowing Omar al Bayoumi-a man from San Diego
108:                heard Hazmi and Mihdhar speaking in what he recognized to be Gulf Arabic and struck
272:                claimed not to remember any specifics of what they discussed. He described Hazmi as
668:            Saudi authorities interviewed the relatives of these men and have briefed us on what
1022:            We have found no evidence that Iran or Hezbollah was aware of the planning for what
1079:                Corridor, but his instructor declined a second request because of what he considered
1355:                money, could not speak English, and could not adequately explain what he intended to
```
This helps to show the line number of file with the line matched. 
