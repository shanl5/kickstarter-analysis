# Kickstarting with Excel

A foundational overview of a tool frequently employed by data scientists to analyze data sets of all sizes (small, medium, large) and introduce analysis topics and other tools of the trade.

## Overview of Project

Analyze crowdfunding campaign data set to advise client "Louise" regarding her prospective play called Fever.

### Purpose

Provide realistic scenario to build upon understanding of methods and tools utilized in many professions including financial advisor and account manager.

## Analysis and Challenges

Depending on particular views into the available data, the recommendation to Louise regarding a funding campaign could vary.

Theater funding has been historically successful in Great Britain<sup>A</sup> -- the data shows nearly 72% (258 of 359) of category campaigns there have been successful (achieved goal or better), but the success rate drops below 60% (515 of 900) if data is considered for category campaigns completed (or canceled) in the US<sup>B</sup>. Yet, if only plays are considered (the theater category includes building space campaigns, a subcategory not applicable to Fever which is to be a play), the subcategory<sup>C</sup> {*in US*}<sup>D</sup> success rate is over 65% (694 of 1066) {*over 61% (412 of 671)*}.

<sup>A,B,C,D</sup> Screenshots in resources.

### Analysis of Outcomes Based on Launch Date

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/106628649/172477482-f2059ac2-d696-4e22-be0f-f52c1e57df51.png)

Reviewing past theater campaigns on the basis of monthly launch timing alone, the recommendation might be to launch a campaign, in any month except December, in which month the number of successful campaigns (37) only barely passes those that failed (35) and is less than half the total (75) launched then. The recommendation to proceed in the other months, however, while especially strong if the campaign is to be launched in the month of May or even June -- where the number of successful campaigns (111 and 100, respectively) about doubles those failed (52 and 49) -- becomes certainly weaker in other months, notably in October, August and January (65, 72, and 56 successful, respectively) -- where more than 40% of the closed theater campaigns failed or were canceled (50+0, 47+4, 33+7). If Louise is to launch a campaign those latter months, the project suggests she may want to devise a special incentive to contributors.

### Analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/106628649/172477611-d847b5e4-d195-46ba-ac66-ee38b42350f8.png)

If the campaign data for the subcategory of plays is set into 12 different groups by size of goal, Louise' campaign of interest (just over $10K) falls into a group where the successful campaigns (39) outnumber failed ones (33) based on the historical data. However, this is only a slim success margin, and going to the next larger-size campaign grouping from there the trend goes downward for success and upward for failure (successful and failed play campaigns both number 12 in the next higher grouping of 15000 to 19999).

### Challenges and Difficulties Encountered

With the large data set of over 4000 records, extensive in terms of industry categories and geographical locations covered, an integral challenge was to distill the data to a pertinent set, while still balancing what not to exclude. Before cells were shaded according to max 90 percentile (mod 1.2.5) rather than by value, another-industry outlier that achieved more than 100K times goal made a difficult task of visualizing the success of non-outlying data cells.
As well, some of the data (e.g. the "deadline" and "launched_at" fields) was not understood at the outset; a formula was provided in the module text as to how to convert these Unix timestamp values to a more easily read date format. Also, on the topic of software preparation, the "Check for Updates" for Module 1.1.1 and what I was seeing on my screen seemed to be out-of-sync; this was resolved via online chat with AskBCS.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

(1) No matter the month launched, a theater crowdfunding campaign can be successful and over the total range of the data (2010-2017) more total have succeeded than failed;
(2) A December campaign launch appears the least likely to be successful of the months.

- What can you conclude about the Outcomes based on Goals?

Going towards the two goal groupings smaller (5000 to 9999, 1000 to 4999) rather than either staying at her current goal range (10000 to 14999) or going into the next two higher groupings (15000 to 19999, 20000 to 24000), would be advisable as *Louise would be more likely to have a successful smaller campaign*.

- What are some limitations of this dataset?

(1) Gaps exist (sparse data) for the category, especially the first four years (2010-2013): no data in 2009; in 2010 only July, October, December (one campaign each); in 2011 March (1 campaign), April (1), December (2); ...
(2) Need more recent data: no data since year 2017.
(3) Could have more data for each of the nine parent categories (film & video, food, games, journalism, music, photography, publishing, technology, theater)

- What are some other possible tables and/or graphs that we could create?

One possibility for a pivot table with associated graph could be the percentage makeup/contribution of outcomes for each category and/or subcategory. This would help to visualize strengths of the data set where a study/analysis might be made.
