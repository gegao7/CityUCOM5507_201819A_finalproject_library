# Harvesting and Analyzing the Library Course Reserve Entries at City University and CUHK —— In Terms of Communication and Sociology

55474073 Qianying YE<br>55383507 Xiaomeng ZHANG<br>55455808 Yiwen SHI<br>55376450 Ge GAO             

Dr. Xinzhi ZHANG

Dec 10, 2018
 
## Introduction
When Hong Kong university students want to know the bibliography specified in the course they are studying, they may refer to the "course reserve" catalog in the library. A course reserve is a service offered to teaching-staffs to make course-related materials available to students and other users in a one-stop-shop manner. Short loan time (5 hours, 1 day or 3 days) for materials in the course reserve are designated by the teaching staff to expedite circulation and give every student the equal opportunity to borrow the relevant bibliography. Such a service is provided by most libraries in Hong Kong universities. 

The course reserve is a significant teaching and learning platform in an academic institution with three main reasons. First, this catalog enables the faculties to pick up their favorite books to share with the students or keep other books that they believe to reflect the milestone pieces of an academic discipline. Second, students can be benefited from such a catalog so that the important books in the field will be always available. Furthermore, a course reserve partly reflects the curriculum design of the departments or schools, it may also demonstrate the intellectual taste of the faculties.

Based on the above causes, this study attempts to scrape the course-reserved entries of communication and sociology of City University of Hong Kong and the Chinese University of Hong Kong (hereafter referred to as CityU and CUHK), as well as perform exploratory data analysis and visualization of the results. 

### 1.1 School Choices: CityU and CUHK
As CityU and CUHK located in Hong Kong with the same social background, the data collected from these two universities are more comparable. Meanwhile, the libraries of the CityU and the CUHK have the same website structure and the same operability, so that the information comparison can be avoided because of the search error. 

### 1.2 Subject Choices: Communication and Sociology
For subject selection, this study have chosen two subjects of communication and sociology. Firstly, as students of the Department of Media and Communication, the researchers of this study have an advantage in the analysis of the subject of communication. There are many intersections between sociology and communication, so we also know more about it and facilitate us to process information. Secondly, the ranks of communication of the two universities are relatively close, while the gap of ranks in sociology rankings are larger. Through such a distinction, it will be more representative that comparing the similar rankings of the same subjects and the different rankings of the same discipline. 

### 1.3 Research Questions
Based on the research background and preliminary analysis of relevant data, this study proposes the following three main research questions.

* Is there any same book between the two universities? If yes, what are their similarities and differences? 

* What is the year of the oldest and newest books? Which school's course-reserved books are newer?

* Is there any author has more than one books have been chosen into course reserve?

Except the above questions, this study decided to explore more. First, by analyzing the amount, year, and theme of the course reserve materials, this study attempts to find out the features of the teaching purposes and the professors' preference. At the same time, the data collected form the library websites can be utilized to compare the difference among the curriculum design, the teaching purpose and the teacher resources between these two universities. Second, by comparing the course-reserved materials of the same subjects in the two university libraries and combining the courses set by the relevant subjects of the two schools, this study can explore the practicality of the library for course learning. Third, the similar course-reserved books provided by the two universities may also reflect the principal needs of market and the changing of media industry, which is also one of the points of interest in this study. Furthermore, since this study compares the subjects with a large disparity in the QS rankings, by analyzing the differences in the course-reserved books, we may be able to find some reasons for this, like curriculum design, teaching purposes.

## Methods
### 2.1 Data Acquisition
#### 2.1.1 Date Source
The source of the data is the library website of CityU and CUHK. There are two main reasons for choosing these two sites as our target sites. First, the two sites have similar architectures so that the similar code can be used to process both sites simultaneously. Second, the content contained in the two sites is comparable because the same search method is utilized to get information.

#### 2.1.2 Variables to be collected 
Since the libraries of the two universities do not directly provide all the course reserves in the two subjects of communication and sociology, this study roughly searched the relevant course reserves contained by each two keywords according to the name of the subject and the nouns mentioned in the field, this can represent the course reserves of the two subjects to a considerable extent. At the same time, to ensure comparability, the same method of searching was conducted for getting the final URL.

The first step was open the official library websites of the two universities and chose the course reserves to retain this option. Next, selected the subject at the search criteria, entered "communication" and "media" separately and chose the button "or" so that the engine can search for the subject containing at least one of these two nouns, which are the keywords of the course reserves of communication science. This research used the same method to search for course reserves roughly included in the subject of sociology in two universities. Social and society are our search keywords. In the end, four URLs containing the relevant information was gained, including the result searched by "`communication`" and "`media`" in [CityU library](https://julac.hosted.exlibrisgroup.com/primo-explore/search?query=sub,contains,communication,OR&query=sub,contains,media,AND&tab=default_tab&search_scope=CourseReserve&sortby=rank&vid=CUH&mode=advanced&offset=0) and in [CUHK library](https://julac.hosted.exlibrisgroup.com/primo-explore/search?query=sub,contains,communication,OR&query=sub,contains,media,AND&tab=default_tab&search_scope=Course&sortby=rank&vid=CUHK&lang=en_US&mode=advanced&offset=0); the result searched by "`social`" and "`sociology`" in [CityU library](https://julac.hosted.exlibrisgroup.com/primo-explore/search?query=sub,contains,social,OR&query=sub,contains,sociology,AND&tab=default_tab&search_scope=CourseReserve&sortby=rank&vid=CUH&mode=advanced&offset=0) and in [CUHK library](https://julac.hosted.exlibrisgroup.com/primo-explore/search?query=sub,contains,social,OR&query=sub,contains,sociology,AND&tab=default_tab&search_scope=Course&sortby=rank&vid=CUHK&lang=en_US&mode=advanced&offset=0).

![Select course reserves, subject and enter the keyword](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/1.png)
<br>Figure 1. Select course reserves, subject and enter the keywords.
 
![The information and variables a book contains](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/2.png)
<br>Figure 2. The information and variables a book contains.

This research decided to compare the development of communication and sociology in the two universities based on the information collected. By analyzing the information contained in the website, this research defined the variables to be analyzed, namely the title, author, version and publication year of a book.
 
![This is the picture of Inspect Element](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/3.png)
<br>Figure 3. This is the picture of Inspect Element.

#### 2.1.3 Procedure
#### Website structure analysis. 
The library websites of the two universities are dynamic websites and have a complicated structure. By reviewing the elements, it seems that the labels of the four variables are highly consistent, which means that the code may not be able to scrape them separately. At the same time, all the information of the whole page can be shown by clicking load more at the bottom of the page.

#### Relevant attempts and basic methods. 
At first, the easiest way was used to scraped tags and paths to get information, but it failed. Then, we tried to use Jason to crack the URL of the original website to get the new URL, but after Python access, the response was 403, which means that the website does not allow access and this method cannot get information. Under the guidance of Dr. Zhang and the teaching assistant, we finally chose to solve the problem of the load more first. After the entire webpage was completely unfolded, it verified that the method of scraping the label to obtain relevant information can be carried out.

Totally, the method this study take is to first use selenium to automatically open the webpage, then click the load more button to load the entire webpage, scraped the content of the tab and get the information. In the process, the main packages this study use was selenium, beautiful soup, and pandas.

#### Difficulties and solutions. 
Although some information was collected through the above methods, more problems appeared. First, in the library website of the CityU, some books have multiple versions and information of these books are folded, only the name of the book and the author can be seen in the webpage, there was no detailed version and year. In this case, if we only scraped this page, some books and information would be overlooked. Furthermore, there is a similar label problem this report mentioned earlier. In the initial stage of scraping, the version and publication year of a book are in the same column and cannot be separated.
 
![The book has multiple versions](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/4.png)
<br>Figure 4. The book has multiple versions.
 
![The same label contains different information](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/5.png)
<br>Figure 5. The same label contains different information.

To solve these two main problems, after trying a variety of methods, the solutions was found.

For the first question, each book in the page has its own separate page link in the target website, and the complete information was contained in the single page, so we divided the scraped into two steps. First, collect links of all books on the page and save them to a CSV file. Second, access the CSV file via Python and use the selenium module to click the links in the file and scraped the information one by one. In this process, setting sleep time and setting functions to implement iterations were two important points.

For the second problem, the code to solve it was to use the number to locate the location of the information contained, and finally successfully segment the year from the version information.

Honestly speaking, due to the influence of network speed, website instability, etc., the information we obtained has some cases of missing years and titles. This situation only appears in the process of scraping the sociology reservations of City University of Hong Kong. In the case where we have been unable to obtain complete information several times and have determined that the code is correct, we have supplemented the missing data by manual filling.
 
![The URLs of each course-reserved book in the field of communication](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/6.png)
<br>Figure 6. The URLs of each course-reserved book in the field of communication.
 
![Screenshot of part of the course-reserved book of Communication Studies at CityU](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/7.png)
<br>Figure 7. Screenshot of part of the course-reserved book of Communication Studies at CityU.

### 2.2 Data Processing
More than one thousand data with four CSV files were scraped totally from library’s websites of CityU and CUHK, and the files contained four columns: title, author, publisher, and publication year. Next, based on our research questions, we explained the procedure of processing data and drawing conclusions from three parts.

#### 2.2.1 The publication year
As mentioned above, with scraping the publishers from websites, the command with “if & else” was used to get the publication year. Then, through the statistics of the number of books in each publication year, the research planned to analyze the current situation of course-reserved books in CityU and CUHK.

Firstly, there were three steps to count the number of course-reserved books in each publication year, including opening, sorting, and counting. The column of “year” was drawn and then sorted values by digital size. In the counting step, a loop command with “for & in” was used to count the number of the same year, which was equal to get the number of publications books in each year. However, for keeping the order of year, the commands were executed in a loop list, resulting in duplicated results as well (showed as Figure 8). Therefore, the research planned to save it as a CSV file and proceed to the next step of data processing.

![The codes of counting the number of books in each year](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/8.png) 
<br>Figure 8. The codes of counting the number of books in each year.

The second step was to drop the duplicate content in the file. An easy command with pandas could achieve the goal, but before this operation, a kind of data cleaning must be handled. Because under the automatic generation of serial numbers, the data of each row was no longer the same so Python could not recognize duplicate content for deletion. Therefore, the deletion of the first column was necessary and the data processing of each subject in each university was completed (showed as Figure 9). Four new CSV files were produced by Python.
 
![The codes of deleting the duplicated data](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/9.png)
<br>Figure 9. The codes of deleting the duplicated data.

Finally, the last step was from processing to visualization. For comparing the annual quantity of books in two universities, the graphic of double-bar was a better choice. However, before generating a chart by Python, there were two significant processing that must be operated. In the beginning, after importing data of the same subject, a new dictionary should be merged in the way of union rather than intersection depending on the common variable “year”. Just as shown in Figure 9, if CityU had no books that published in 1966 but CUHK has one, “NaN” which meant not a number would be picked up in the blank. Since the order of the merger was based on the column of the first file, i.e. the publication year of CUHK, as mentioned in Figure 10, the years that CityU had books but CUHK has nothing were arranged at the end, which was not conducive to visualize. So another sorted command should be drawn, the final nice figure was generated by Python (showed as Figure 11)

![The codes of merging data](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/10.png) 
<br>Figure 10. The codes of merging data.

![The problem of merging data](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/11.png)
<br>Figure 11. The problem of merging data.

 ![The visualization pf publication years](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/12.png)
 <br>Figure 12. The visualization pf publication years.

#### 2.2.2 The keywords of titles
From our perspective, the title of course-reserved books can directly show the emphasis of courses in CityU and CUHK. With the scarping of books’ titles, the research draws the keywords of them and shows the statistics results, revealing as Figures of World Cloud.

There were three necessary data processing before visualization. Firstly, the words from titles need to be removed from stop words, which including “and”, “or”, “this” and so on. But as cleaned for the first time, it was found that punctuations were not dropped, causing the most frequency keywords is the colon. Then a list of commonly used punctuations was added to the package of stop words and complete the first cleaning step (showed as Figure 13).

![The codes of deleting stop words](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/13.png) 
<br>Figure 13. The codes of deleting stop words.

The second step is to count the repeated keywords. However, the capitals and lower letters are not unified which will cause counting in a mistake. An easy loop command was used and a new list that contained all lower letters was created. This new list was prepared to be saved as txt file, which was the material for visualization. In addition, it is necessary to count the keywords in the new list with the same method as the processing of publication year. After sorting the keywords by the number of them, an ascending order occurred and although the most frequency words could be seen at the end of the queue, all the accurate and clear outcomes was born.

The last step is to generate figures of Word Cloud by installing a package in Python. With the tutorial online, nice Word Cloud was successfully made, especially making the user-defined font, background, color, shape and so on. Two universities logos were chosen as the shape and color of Word Cloud to add features and help to contrast clearly (showed as Figure 14).
 
![The codes of generating Word Clouds](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/14.png)
<br>Figure 14. The codes of generating Word Clouds.

#### 2.2.3 The overlapping books of CityU and CUHK
The third part of data processing was the most challenging and difficult for the research, although it looked like the simplest one. And frankly speaking, it did not complete in the end.

The last goal was to compare the same books with the same subject of two universities. To achieve, there were two steps that need to capture. Firstly, finding the same books while secondly, drawing the same books with other information, containing authors and publishers.

Initially, the column of titles was drawn by importing the CSV file and found the overlapping book through the loop command. Unfortunately, there was a big problem in the second step. Although the information of the overlapping book was found in the respective CSV source files of CityU and CUHK, it could not be converted into a complete form. It can only be displayed in Python as shown in Figure 15, and the displayed content was also confusing. The outcome was tried to export the CSV files directly, but only the last row of data could be displayed. After searching online, it could be guessed that the loop covers the previous one, but our group had not solved this problem after a long period of effort.
  
![The codes of searching the same information](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/15.png)
<br>Figure 15. The codes of searching the same information.

Then after searching a lot online and asking somebody who majored in computer science, the tutor guided another way with the concept of defaultdict. In fact, defaultdict is a dictionary as well, but Python automatically assigns an initial value to its key then it can reduce errors. Our tutor helped us to define a command with two steps of finding and collecting, and finally export in one CSV files with all information. The whole codes were clearly for understood but a little difficult for us to write (showed as Figure 16). Furthermore, a step of data cleaning was included in the entire codes, dropping the index and the headline.

To sum up, while some processing the research had not achieved absolutely, most of them were completed in our efforts. And it is believed that our group will be more and more skilled at Python and solve the problems we did not solve today.
 
![The entire codes of finding overlapping books by the tutor](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/16.png)
<br>Figure 16. The entire codes of finding overlapping books by the tutor.

## Results
Based on the data acquired from the websites, the differences between the course reserve materials from City University and CUHK are obvious.

Firstly, overall speaking, there is a considerable difference in the number of total course reserve books from both the communication section and the sociology section between these two universities. CityU has 337 volumes of communication-related reserve books and 53 volumes of sociology related reserve books, while CUHK has 532 reserve books of communication section and 132 reserve books of sociology section. The total amount of books from CUHK is about twice as much as the number of books from CityU. But from table 1 below, it indicates that each teaching staff of CityU in communication has 6.2 course reserve books. Even though there are fewer reserve books of sociology section in CityU library, the mean amount of reserve books for each teaching stuff is about the same with which of CUHK.

Table 1. The overall analysis about course reserve books<br>
![The overall analysis about course reserve books](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/table2.png)

Then, the editions of the same books were compared by searching the same book titles. Due to different curriculum setting, there are only a few overlapping books of these two subjects between these two universities. There are 24 overlapping books in sociology section and only 3 overlapping books in the communication section. In general, the course reserve books from CityU library mainly cover only one edition, usually the newer edition. As for books from CUHK library, there is usually more than one edition, including one newest edition and older editions. These editions collected by CityU library are also collected by the CUHK library. 

Furthermore, according to the course setting, the courses of City university tend to focus more on the newest research fields, so we supposed that the reserve books of CityU library are published later than those of CUHK library. 

Table 2. The number of books of communication science in every publishing year<br>
![The number of books of communication science in every publishing year](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/table3.png) 

Table 3. The number of books of sociology in every publishing year<br>
![The number of books of sociology in every publishing year](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/table4.png)

From Table2 and Table3, it's obvious that in terms of the larger total amount, the publish year of the reserve books in CUHK distribute wider. As for course reserve books related to the communication field, the publishing years of the books in CityU range from 1990, while the publishing years of the books in CUHK range from 1966. There are 7 volumes of books of CUHK in communication filed published before 1990. In sociology field, the publishing years of the reserve books in CityU mainly covers later from 1980, while in CUHK from 1931. There are 10 course reserve books published before 1980 in sociology field collected by CityU library, while there are 27 books collected by CUHK library. There is no evidence to prove that the reserve books of CityU library are newer than those of CUHK library, but the collections in CityU library are published mainly in the recent decades.

Besides, top ten most commonly appearing words in the book titles were discovered in these two subjects of each university. The top title words in the communication-related reserves books in CityU are communication, media, marketing, communications, guide, mass, technology, integrated, research, human and culture; in CUHK are language, communication, legal, writing, acquisition, cultural, introduction, culture, studies, and guide.  The word clouds show that there are many common issues discussed in the reserve books, such as mass communication and cultural phenomenon. But the differences are also obvious. The courses of communication subject in CUHK covers more language acquisition and writing, while CityU focuses more on practical issues about integrated marketing.
  
![The word clouds of book titles in communication field of two universities](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/18-1.png)
![The word clouds of book titles in communication field of two universities](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/18-2.png)
<br>Figure18. The word clouds of book titles in communication field of two universities.

As for reserve books of sociology, there are some similar words commonly appearing in the titles, such as society, research, political and so on. However, the courses of sociology in CUHK focus more on the social works on the macro level (Hong Kong and China etc.); in contrast, sociology courses in CityU emphasis more on the issues about social communities.
  
![The word clouds of book titles in sociology field of two universities](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/19-1.png)
![The word clouds of book titles in sociology field of two universities](https://github.com/gegao7/CityUCOM5507_201819A_finalproject_library/blob/master/Harvesting%20and%20Analyzing%20the%20Library%20Course%20ReserveEntries%20at%20City%20University%20and%20CUHK%20%E2%80%94%E2%80%94%20In%20Terms%20of%20Communication%20and%20Sociology/19-2.png)
<br>Figure19. The word clouds of book titles in sociology field of two universities.

## Conclusions and Implications
We collected the data of reserve books by searching the keywords and analyzed the basic information of all the books to see the similarities and differences of the reserve books of these two universities, then to find out the differences of the curriculum design.

In all, firstly compared with CUHK, City University is slightly inferior in the scale and amount of university library collection. CUHK provides students with more kinds of books and more different editions of the books. For a wide range of reasons, the scale of City University library is relatively smaller, so there is not much space for lecturers to recommend more reserve books. However, since students can borrow the books from other university libraries online as JULAC card holders, their academic needs can be almost totally satisfied.

Secondly, by deep analysis of the book titles, it can be concluded that the structures of the curriculum system of these two universities in subject communication and sociology differ from each other. CUHK's courses focus more on the theoretical research, which involves most problems in macro level; City U's courses, in contrast, concentrate more on practical studies. It may also explain why lecturers recommend fewer books as course-reserved books (i.e., the textbooks).

Compared with the traditional courses related to communication science still concentrating on the traditional media, in the recent years, City University has established new streams, such as Media Data Analytics Stream, and a series of courses aiming at providing knowledge about cutting-edge media technologies for professionals working in the communication science fields. But in fact, when we analyzed the titles of the books, we found that there are not enough books relevant to the advanced communication science studies in the list. Thus, the relevant reserve books list should be updated and some books about new media, advanced media technologies can be added to the list. Although the classic works should be attached much importance to, students also need to obtain more knowledge from some newer aspects.

## Limitations

Due to the lack of technical competence, there are some limitations of this study. 

First, the data sources of this study are not comprehensive. This study only chose two majors of liberal arts, no other kinds of subjects like science, business studies etc, and did not compare the overall situation between the two universities in maintaining bibliography at a macro level. 

Second, the processing of the data is not deep enough. That is why this study did not make use of the information which we have scraped from the websites. This study did not figure out how to collect information about publishing countries of the books from author names and publishers. If this problem can be solved, this study can find more points that can be analyzed and compared of the course-reserved books between these two universities.
 
## References
The online tutorials we used:
1.	https://blog.csdn.net/qq284489030/article/details/79507161
2.	https://www.cnblogs.com/duyang/p/5065418.html
3.	https://www.jb51.net/article/115578.htm
4.	https://blog.csdn.net/ly_ysys629/article/details/73849543
5.	https://blog.csdn.net/erinapple/article/details/79332780
6.	https://blog.csdn.net/qq1483661204/article/details/79824381
7.	https://blog.csdn.net/sinat_29957455/article/details/78993732
8.	https://www.jb51.net/article/104924.htm
9.	https://baijiahao.baidu.com/s?id=1604046091238853462&wfr=spider&for=pc
10.	https://www.jb51.net/article/116346.htm
