# The assignment is hosted at [shiny.reidmcy.com/ntg](http://shiny.reidmcy.com/ntg/)

It's on my own small server so if it's not responding you can run the it from `dash.Rmd`.

## Discussion

The goal of the app is to let people explore and compare the records, and is going to be the starting point for a deeper analysis of the models. The flexbox engine means that space is limited so while I considered reducing font sizes and putting everything together, I decide, after testing, the results would be too ugly and unreadable on small displays.

The data for the app are 600 scientific article's titles, abstracts and other metadata. They are part of the 1.5 million used in my thesis, and were picked as a representative sample.

The app presents users with the ability to select a subject then one or two records from the subject. The option to select only one was done to allow viewing multiple tabs more easily. This is meant as an exploratory visualization so as much data as possible is shown, since I do not know ahead of time what is relevant.

The first tab of the viewers give the title, base classification and model predictions. This is given first as it will be the most important information when comparing records. The second tab is the abstract, as a human would see it, the abstract and title are the only things the models see so the abstract is the second most important piece of information. The metadata and subjects fields give additional information about the record, helping the reader understand the record's place. The last two tabs are the parts of speech tagged title and abstract. These are more inline with how the model views them and thus give more insight into how it works.

My original layout and interactive flows for this app are impossible in flexdashboard (and probably shiny) so getting something that was possible and was copacetic was a challenge. Additionally the need to go straight to raw html for most UI was time consuming and led to receptive coding. Finally the tokenizer and POS tagger are difficult to install, so if you are trying to run this on your own machine, good luck.
