# NationStates-Stats
Data extraction and Analysis for NationStates' Nation Stats.

## About NationStates
From its homepage: NationStates is a nation simulation game. Create a nation according to your political ideals and care for its people. Or deliberately oppress them. It's up to you.

So one of the aspects of the game involve Issues, whereby you answer issues and problems that pop up on your nation. These have positive and negative impacts on your nation's statistics, depending on your choice.

It came with the very first question I had: By *how* much does Integrity change with Authoritarianism (attribute of being a dictatorship)?

I have written more about it here as part of NationStates' Great Exhibition 2021: https://nsge.jcink.net/index.php?showtopic=72.

## How to run - the very barebones version.
The requirements.txt install.

Run the Data Extractor and Cleaner - WARNING: For some versions of Jupyter Notebook, it has a habit of using a lot of RAM (and slowing Firefox (not sure about other browsers) down) to a large degree for a while. I suspect it has something to do with getting all 300,000+ nation names, but this did not happen before on older Jupyter Notebook versions. A sample of 20 rows of data, extracted on 2024-10-26, is provided.

The Cleaner will remove away Null or NA nations - this does NOT include nations whose rank has the same value as the data itself. As long as the stats are intact, it will still be inside. The N/A nations in this case are CTE'd nations. The cleaning part also removes commas from the policy description (some of them still has a comma, for example, the No Smoking even in private areas one.)

The .csv file will then be generated, after which use your favorite SQL method to, well, add this data into SQL. I used MySQL for reference.

If all goes well, then you can then use MySQL (can be others depending on what you use) by connecting to your database. This significantly reduced the time from 10 minutes to 10 seconds, since you are only loading essential data. 

SKIP the Gaussian KDE if you either do not want it, or that you have already run before. I have added a part whereby it will keep two .out files that can be loaded back easily. TODO / WARNING: There is NO overwrite protection so if you ran the Gaussian KDE and you realized that you have done it before, you have around 2500 seconds to stop the script before it overwrites.

## Credits
Various credits are given in each of the snippets where I have taken some ideas here and there from StackOverflow. And my many thanks to people from and outside of NationStates for helping me out with coding, support, or inspirations.
