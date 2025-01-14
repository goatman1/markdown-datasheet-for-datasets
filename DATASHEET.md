# Datasheet: Google Trend: Diet v.s. Gym

Author: *Minghao chen*

Organization: *University of Michigan*

Google Trend analyzes the popularity of top search queries in Google Search across various regions and languages. In its website, graphs are used to compare the search volume of different queries over time. Originally, Google neglected updating Google Trends on a regular basis. In March 2007, internet bloggers noticed that Google had not added new data since November 2006, and Trends was updated within a week. Google did not update Trends from March until July 30, and only after it was blogged about, again.Google now claims to be "updating the information provided by Google Trends daily; Hot Trends is updated hourly."

In 2009, Yossi Matias et al. published research on the predictability of search trends.[1] In a series of articles in The New York Times, Seth Stephens-Davidowitz used Google Trends to measure a variety of behaviors. For example, in June 2012, he argued that search volume for the word "nigger(s)" could be used to measure racism in different parts of the United States. Correlating this measure with Obama's vote share, he calculated that Obama lost about 4 percentage points due to racial animus in the 2008 presidential election.[2] He also used Google data, along with other sources, to estimate the size of the gay population. This article noted that the most popular search beginning "is my husband" is "is my husband gay?"[3] In addition, he found that American parents were more likely to search "is my son gifted?" than "is my daughter gifted?" But they were more likely to search "is my daughter overweight?" than "is my son overweight?"[4] He also examined cultural differences in attitudes around pregnancy.[5]

This dataset consider how searches for the terms "diet" and "gym" vary from September 3, 2005 to October 3, 2020, to analyze the potential regulation of people's behaviors behind the data.

## Motivation


1. **For what purpose was the dataset created?** Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description.

	*To analyze the potential regulation of people's behaviors behind the data and then advise the markets*

2. **Who created this dataset (e.g. which team, research group) and on behalf of which entity (e.g. company, institution, organization)**?

	*Minghao Chen based on Google Trend*

3. **What support was needed to make this dataset?** (e.g. who funded the creation of the dataset? If there is an associated grant, provide the name of the grantor and the grant name and number, or if it was supported by a company or government agency, give those details.)

	*Access to Google Trend*

4. **Any other comments?**

	*Google Trend started from 2005, therefore, our data started from 2005*


## Composition


1. **What do the instances that comprise the dataset represent (e.g. documents, photos, people, countries)?** Are there multiple types of instances (e.g. movies, users, and ratings; people and interactions between them; nodes and edges)? Please provide a description.

	*Google Trend consists of numerical and text files. Countries represent the location, date represent the recorded time, and gym and diet represent the search times of the date*

2. **How many instances are there in total (of each type, if appropriate)?**

	*There are 40 countries, 2 types of trend (gym and diet), 181 dates (from 2005 Oct to 2020 Oct) in total.*

3. **Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?** 

	*The dataset only compares gym and diet. There are many other Trends of key words in the website. Also, it samples the Oct 2005 to Oct 2020, but the latest Trend data is to today.*

4. **What data does each instance consist of?** "Raw" data (e.g. unprocessed text or images) or features? In either case, please provide a description.

	*Text for courties: China*
	*Number for dates: 2020-10-05*
	*Text for Trend type: Gym*
	*Number for Trend: 65*

5. **Is there a label or target associated with each instance?** If so, please provide a description.

	*No*

6. **Is any information missing from individual instances?** If so, please provide a description, explaining why this information is missing (e.g. because it was unavailable). This does not include intentionally removed information, but might include, e.g. redacted text.

	*No.*

7. **Are relationships between individual instances made explicit (e.g. users' movie ratings, social network links)?** If so, please describe how these relationships are made explicit.

	*These two Trends might be correlated.*

8. **Are there recommended data splits (e.g. training, development/validation, testing)?** If so, please provide a description of these splits, explaining the rationale behind them.

	*PCA analysis, Deep learning model.*

9. **Are there any errors, sources of noise, or redundancies in the dataset?** If so, please provide a description.

	*Early data might be noisy since Google did not update it daily until 2008. Therefore, some previous data might come from the regression or miss some information.*

10. **Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g. websites, tweets, other datasets)?** If it links to or relies on external resources, a) are there guarantees that they will exist, and remain constant, over time; b) are there official archival versions of the complete dataset (i.e., including the external resources as they existed at the time the dataset was created); c) are there any restrictions (e.g. licenses, fees) associated with any of the external resources that might apply to a future user? Please provide descriptions of all external resources and any restrictions associated with them, as well as links or other access points, as appropriate.

	*The dataeset is from Google Trend: https://trends.google.com/trends/explore?date=2005-09-04%202020-10-04&q=diet,gym.*

11. **Does the dataset contain data that might be considered confidential (e.g. data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals' non-public communications)?** If so, please provide a description.

	*No, all data comes from public open source.*

12. **Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?** If so, please describe why.

	*No.*

13. **Does the dataset relate to people?** If not, you may skip the remaining questions in this section.

	*Yes, it reveals how poeple search the gym or diet in the past few years.*

14. **Does the dataset identify any subpopulations (e.g. by age, gender)?** If so, please describe how these subpopulations are identified and provide a description of their respective distributions within the dataset.

	*Yes, by regions.*

15. **Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?** If so, please describe how.

	*No.*

16. **Does the dataset contain data that might be considered sensitive in any way (e.g. data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?** If so, please provide a description.

	*Yes, it might lead some religous beliefs since the dataset is sorted by region.*


## Collection

*As with the previous section, dataset creators should read through these questions prior to any data collection to flag potential issues and then provide answers once collection is complete. In addition to the goals of the prior section, the answers to questions here may provide information that allow others to reconstruct the dataset without access to it.*

1. **How was the data associated with each instance acquired?** Was the data directly observable (e.g. raw text, movie ratings), reported by subjects (e.g. survey responses), or indirectly inferred/derived from other data (e.g. part-of-speech tags, model-based guesses for age or language)? If data was reported by subjects or indirectly inferred/derived from other data, was the data validated/verified? If so, please describe how.

	*From Google Trend website*

2. **What mechanisms or procedures were used to collect the data (e.g. hardware apparatus or sensor, manual human curation, software program, software API)?** How were these mechanisms or procedures validated?

	*Python API*

3. **If the dataset is a sample from a larger set, what was the sampling strategy (e.g. deterministic, probabilistic with specific sampling probabilities)?**

	*Deterministic*

4. **Who was involved in the data collection process (e.g. students, crowdworkers, contractors) and how were they compensated (e.g. how much were crowdworkers paid)?**

	*Google users and developers*

5. **Over what timeframe was the data collected?** Does this timeframe match the creation timeframe of the data associated with the instances (e.g. recent crawl of old news articles)? If not, please describe the timeframe in which the data associated with the instances was created. Finally, list when the dataset was first published.

	*From Oct 2005 to Oct 2020, which matches the creation time frame of the data.*

7. **Were any ethical review processes conducted (e.g. by an institutional review board)?** If so, please provide a description of these review processes, including the outcomes, as well as a link or other access point to any supporting documentation.

	*No.*

8. **Does the dataset relate to people?** If not, you may skip the remainder of the questions in this section.

	*Yes.*

9. **Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g. websites)?**

	*From Google the third party.*

10. **Were the individuals in question notified about the data collection?** If so, please describe (or show with screenshots or other information) how notice was provided, and provide a link or other access point to, or otherwise reproduce, the exact language of the notification itself.

	*No, this dataset comes from shared users behaviors.*

11. **Did the individuals in question consent to the collection and use of their data?** If so, please describe (or show with screenshots or other information) how consent was requested and provided, and provide a link or other access point to, or otherwise reproduce, the exact language to which the individuals consented.

	*Yes, every Google user accept the statements for sending data to Google for better service.*

12. **If consent was obtained, were the consenting individuals provided with a mechanism to revoke their consent in the future or for certain uses?** If so, please provide a description, as well as a link or other access point to the mechanism (if appropriate).

	*Yes, people can uninstall the Google service.*

13. **Has an analysis of the potential impact of the dataset and its use on data subjects (e.g. a data protection impact analysis) been conducted?** If so, please provide a description of this analysis, including the outcomes, as well as a link or other access point to any supporting documentation.

	*No.*

14. **Any other comments?**

	*The dataset is automatically updated every day.*


## Preprocessing / Cleaning / Labeling

*Dataset creators should read through these questions prior to any pre-processing, cleaning, or labeling and then provide answers once these tasks are complete. The questions in this section are intended to provide dataset consumers with the information they need to determine whether the “raw” data has been processed in ways that are compatible with their chosen tasks. For example, text that has been converted into a “bag-of-words” is not suitable for tasks involving word order.*

1. **Was any preprocessing/cleaning/labeling of the data done (e.g. discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?** If so, please provide a description. If not, you may skip the remainder of the questions in this section.

	*Yes, the dataset has been classified and labelled by Google.*

2. **Was the "raw" data saved in addition to the preprocessed/cleaned/labeled data (e.g. to support unanticipated future uses)?** If so, please provide a link or other access point to the "raw" data.

	*Yes but it might not be for public access. It should be stored in Google internal dataset.*

3. **Is the software used to preprocess/clean/label the instances available?** If so, please provide a link or other access point.

	*Python and Google cloud.*

4. **Any other comments?**

	*Though it has been labeled by Google first, people can relabel it for their own purposes.*


## Uses

*These questions are intended to encourage dataset creators to reflect on the tasks  for  which  the  dataset  should  and  should  not  be  used.  By  explicitly highlighting these tasks, dataset creators can help dataset consumers to make informed decisions, thereby avoiding potential risks or harms.*

1. **Has the dataset been used for any tasks already?** If so, please provide a description.

	*Yes, it was adopted as training data for a Machine Learning model to predict search trends for the 12-month period starting October 1, 2020.*

2. **Is there a repository that links to any or all papers or systems that use the dataset?** If so, please provide a link or other access point.

	*Yes.*

3. **What (other) tasks could the dataset be used for?**

	*It might also be used to consider the correaltion between two trends. For example, covariance analysis.*

4. **Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?** For example, is there anything that a future user might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g. stereotyping, quality of service issues) or other undesirable harms (e.g. financial harms, legal risks) If so, please provide a description. Is there anything a future user could do to mitigate these undesirable harms?

	*Be carefully in splitting the data for training and predicting. The periodic charactersitic is important when processing the dataset.*

5. **Are there tasks for which the dataset should not be used?** If so, please provide a description.

	*Predict future search trends. Marketers often use such predictions to decide how to allocate their marketing budget. *


## Distribution

*Dataset creators should provide answers to these questions prior to distributing the dataset either internally within the entity on behalf of which the dataset was created or externally to third parties.*

1. **Will the dataset be distributed to third parties outside of the entity (e.g. company, institution, organization) on behalf of which the dataset was created?** If so, please provide a description.

	*Yes, every one with access to Google is eligible for using this dataset.*

2. **How will the dataset will be distributed (e.g. tarball on website, API, GitHub)?** Does the dataset have a digital object identifier (DOI)?

	*By website.*

3. **When will the dataset be distributed?**

	*Anytime.*

4. **Will the dataset be distributed under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?** If so, please describe this license and/or ToU, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms or ToU, as well as any fees associated with these restrictions.

	*Yes, the dataset's copyright by Google.*

5. **Have any third parties imposed IP-based or other restrictions on the data associated with the instances?** If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms, as well as any fees associated with these restrictions.

	*In my knowledge, no.*

6. **Do any export controls or other regulatory restrictions apply to the dataset or to individual instances?** If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any supporting documentation.

	*No.*

## Maintenance

*As with the previous section, dataset creators should provide answers to these questions prior to distributing the dataset. These questions are intended to encourage dataset creators to plan for dataset maintenance and communicate this plan with dataset consumers.*

1. **Who is supporting/hosting/maintaining the dataset?**

	*Google Inc.*

2. **How can the owner/curator/manager of the dataset be contacted (e.g. email address)?**

	*Google.com.*

3. **Is there an erratum?** If so, please provide a link or other access point.

	*No.*

4. **Will the dataset be updated (e.g. to correct labeling errors, add new instances, delete instances)?** If so, please describe how often, by whom, and how updates will be communicated to users (e.g. mailing list, GitHub)?

	*Yes, by Google, updated everyday.*

5. **If the dataset relates to people, are there applicable limits on the retention of the data associated with the instances (e.g. were individuals in question told that their data would be retained for a fixed period of time and then deleted)?** If so, please describe these limits and explain how they will be enforced.

	*No.*

6. **Will older versions of the dataset continue to be supported/hosted/maintained?** If so, please describe how. If not, please describe how its obsolescence will be communicated to users.

	*Yes.*

7. **If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so?** If so, please provide a description. Will these contributions be validated/verified? If so, please describe how. If not, why not? Is there a process for communicating/distributing these contributions to other users? If so, please provide a description.

	*Yes they can contact Google.*

## Reference
	
 [1]On the predictability of Search Trends, Yossi Matias, Niv Efron, and Yair Shimshoni, Insights Search, Google Research blog, August 17, 2009.
 
 [2]Stephens-Davidowitz, Seth. "How Racist Are We? Ask Google". The New York Times.
 
 [3]Stephens-Davidowitz, Seth. "How Many American Men Are Gay?". The New York Times.
 
 [4]Stephens-Davidowitz, Seth. "Tell Me, Google. Is My Son a Genius?". The New York Times.
 
 [5]Stephens-Davidowitz, Seth. "What Do Pregnant Women Want". The New York Times.
