# NationStates-Stats
Data extraction and Analysis for NationStates' Nation Stats.

## About NationStates
From its homepage: NationStates is a nation simulation game. Create a nation according to your political ideals and care for its people. Or deliberately oppress them. It's up to you.

So one of the aspects of the game involve Issues, whereby you answer issues and problems that pop up on your nation. These have positive and negative impacts on your nation's statistics, depending on your choice.

It came with the very first question I had: By *how* much does Integrity change with Authoritarianism (attribute of being a dictatorship)?

I have written more about it here as part of NationStates' Great Exhibition 2021: https://nsge.jcink.net/index.php?showtopic=72.

## How to run
Simply ensure that you have the required packages, the attached data, and it should be good to go. Please do note that the data is limited to 50,000 nations due to the sheer size.

## Data Extractor
As part of freedom of data and to help everyone involved, I have recently added the Data Extractor that I have used and refined eventually in order to get the data I need.

Please note that putting the raw .csv into the Analyser does not work for the time being. I still have some TODOs, in particular: Data is raw and will need small touches on Excel - removing quotation marks, adding Adjusted Economic Freedom, etc. I would recommend that you use the data I provided; this is more of me posting this code so that those who want to can do it at home. ^^

Adjusted Economic Freedom's quick formula: If Economic Freedom < 0, add 100. If it is 0, 50 for now (it currently ignores Communist/Capitalist policies, another to-do!). If Economic Freedom > 0, leave it.

## Credits
Various credits are given in each of the snippets where I have taken some ideas here and there from StackOverflow.
