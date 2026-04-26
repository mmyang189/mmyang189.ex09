---
# Do not edit the text between these lines!
layout: default
---

# Assignment overview

Exams (quizzes) are generally one of the most stressful periods within any course throughout the semester, as they often take up a heavy portion of one's grades and test the retained skills of each student across the content that has been covered (thus far). Therefore, it is imperative, at least for the success of many, to prepare well for such exams: as through means of content review or applied practice. 

As of writing, the current format for review is fairly limited to asynchronous lecture assignments, challenge questions, programming exercises, and one quiz-review session a few days before the quiz. While these are plenty, the current layout may be insufficient for effective quiz preparation. 

Additionally, different majors have different course requirements and applications within their field. An approach to data analysis I will be taking is looking into how metrics of difficulty, pre-lecture video preference, and quiz prep effectiveness change depending on the major of the student enrolled.

My idea of potentially improving the course is that it should implement more asynchronous resources such as pre-lecture videos and quiz-runthroughs to effectively help busy/struggling students personalize their studying practice.

<!-- This is a comment. Below, you'll see code for inserting an image. To make this image appear, update <custom-path>. To add an image, save it inside the imgs folder of this repository. -->
<img src="static\imgs\logo.png" alt="Image of Comp110 rainbow logo. "  width="500"/>

## Code Analysis

To address the idea, "The course should implement more asynchronous resources...", I need to import the data to represent currently enrolled student sentiment regarding current resources. I will then use the columnar function to convert rows to columns, which simplifies accessing specific data across entire datasets into a single list. Finally, the head function will be implemented to check the integrity and organization of the data before conducting the entire analysis.

Once all our data is imported and cleaned, I will use the select function to narrow the table down to feature columns of interest, which include pre_lecture_videos, qz_effective, difficulty, and major. 

Next, I'll implement the count function to determine the amount of each major currently enrolled in the course. To make the most out of it, I'll also implement code to sort out the five most frequent majors based on their count values, which will be important in analyzing data relative to specific majors. To check whether or not the code had an intended output, I added a print statement at the bottom to find the names of the common majors and the number of responses. 

The custom helper function used for this assignment is only_major. This will be used to filter rows of a specific major, which allows us to create a new table that contains information for the top five most frequent majors we want to look at. Additionally, instead of simply discarding the rest of the unused data, I wanted to group other less prominent majors into their own group (Other), to add to the comparison.

Because I plan on creating visuals that directly compare trends among the most frequent majors, I'll also use only_major to filter out the specific majors. Finally, concat will be used once more to create the final data table used to create the graphs.

Visuals that will be looked at are:
1. Line plots for general trend of difficulty compared to either quiz preparation effectiveness or pre-lecture videos.

<img src="static\imgs\class_difficulty_quizeffect.png" alt= "Class Data of Quiz Prep Effectiveness vs. Difficulty. " width="500">


<img src="static\imgs\class_difficulty_videos.png" alt= "Class Data of Pre-lecture Video Preference vs. Difficulty. " width="500">

2. A bar chart to compare average difficulty ratings of the class in the five most common majors and other majors.

<img src="static\imgs\major_comparison_bars.png" alt= "Average Difficulty Scores by Ranked Majors. " width="500">

3. Line plot comparing difficulty with pre-class videos or quiz preparation across the five most common majors.

<img src="static\imgs\difficulty_quiz_effectiveness_comparison.png" alt= "Quiz Prep Effectiveness vs. Difficulty for Top Five Majors. " width="500">

<img src="static\imgs\difficulty_video_preference_comparison.png" alt= "Pre-lecture Video Preference vs. Difficulty for Top Five Majors. " width="500">


## Conclusion

The general data depicts a positive correlation between the use of pre-lecture videos and difficulty, suggesting that as students find the material more challenging, they increasing rely on asynchronous video resources. Conversely, there is also a negative correlation between perceived difficulty and quiz preparation effectiveness. Specifically, students who rated the course difficulty higher (around 7) generally reported lower ratings for how effective their quiz preparation was. This indicates a potential gap in resources that may not be sufficient for students to find comfort in the class, necessitating more targeted investment in preperatory material.

After filtering out the five most common majors of enrolled students (neuroscience, biology, business, economic, and data science), the bar plot revealed that Biology and Business majors expressed slightly higher mean difficulties (4.54 and 4.47 respectively) compared to other majors (ranging from 4.15 to 4.30). While the differences are subtle, they suggest that students in these traditionally non-computational fields may experience hurdles in translating their knowledge onto more logic-heavy concepts explored in COMP110.

The final line plots comparing specific major trends support the idea that major is not a strong influence over success, as there was high variance in linear trends across all abundant majors. This shows that student experiences are diverse even within a single department. However, some lines depict a similar trend to the general data plots, which could emphasize a bit of consistency with how quiz preparation may need to be refined, and how pre-lecture videos may assist students in reducing their perceived difficulty.

With all this in mind, the results seem to agree with the premises of my proposed idea. Students increasingly depend on asynchronous resrouces like pre-lecture videos as the course complexity grows. While further data on prior experience and foundational understanding could have provided a more granular look at why certain students struggle, the current data suggests that the "value gap" is greater at higher difficulties. My recommendation is to develop and provide "review modules" that record logic-heavy concepts in areas where quiz effectiveness may be lacking. 

While it may be a ways off to fully entice students to watch videos, an approach that could be made is to incentivize viewing videos for credit. A potential trade-off is that is may create more "busy work" for students who can effectively understand and review the course material, potentially decreasing the overall satisfaction with the course. The stakeholders most negatively impacted would be those with programming experience who don't require as much foundational development as some of their peers. Furthermore, teaching teams and instructors may also face the cost of increased technical management and time commitment to push and verify asynchronous engagement.