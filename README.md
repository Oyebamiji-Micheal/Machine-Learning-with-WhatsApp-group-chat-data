<h1>Machine Learning with WhatsApp group chat data</h1>
<p>Exploratory and predictive analysis of WhatsApp group chat data</p>

<h2>Table of Contents</h2>

- [Project Description](#description)
- [The Dataset](#dataset)
- [Data Wrangling](#wrangling)
- [Exploratory Data Analysis](#eda)
- [Predictive Data Analysis](#predict)

<a id="description"></a>
<h2>Project Description</h2>
This project is targeted at practicing basic data science processes which include   

- File handling 
- Data preparation or wrangling using the Pandas module, regular expression and common Python functions
- Data Visualization using Matplotlib, Seaborn, Plotly and so on 
- Machine Learning with time series data
- Documentation and Deployment 

<a id="dataset"></a>
<h2>The Dataset</h2>
<p align="justify">This dataset was exported from a WhatsApp group(hey I'm in the group) and is dated 21st of August 2021 through 7th of November 2022.
<br>  
<strong>Disclaimer: </strong> This dataset is solely attributed to learning. All messages and names are frictional; any resemblance to the context/name of a person, organization, group, institution is purely coincidental. I shall not be liable for, and specifically disclaims any warranties in connection with the interpretation and use of the dataset. Thank you!
</p>

```
The txt file looks like this
Let's send out🔥🔥🔥
9/17/21, 8:04 PM - +234 ***: Done boss🙌🙌🙌
9/17/21, 8:07 PM - +234 ***: Pls is pet engineering under faculty of science??
9/17/21, 8:07 PM - +234 ***: ????
9/17/21, 8:08 PM - +234 ***: Tech
9/17/21, 8:08 PM - +234 ***: Thanks boss
```

<a id="wrangling"></a>
<h2>Data Wrangling</h2>
<p align="justify">The dataset contains four important attributes: date, time, author and message. With the exception of messages which spawns across multiple lines, each line of a typical exported WhatsApp data contains the date and time a message was sent along with its corresponding author; and of course the message too. Some lines of text however are not messages sent by an author but by WhatsApp. For example, the message '11/16/21, 10:31 AM - John joined using this group's invite link' means a particular user joined the group on the specified date - this is actually not sent by the user. A similar trend is seen when someone leaves a group or changes their mobile number and so on. How these cases are handled along with how the attributes are parsed and extracted can be found <a href="https://github.com/Oyebamiji-Micheal/Machine-Learning-with-WhatsApp-group-chat-data/blob/main/wrangle.ipynb">here</a>.  
</p>

The first five rows of the wrangled data are shown below

date |	time	|   name    |	message
|:--:|:--------:|----------:|:--------:|
0 |	2021-08-22 |	08:21:00 |	Skillup |	Please someone should post the compiled zoom t...
2 |	2021-08-22 |	17:07:00 |	Rufus |	https://arcg.is/0nyGPD0 The online medical ...
3 |	2021-08-22 |	17:08:00 |	Rufus |	This stuff is long now
4 |	2021-08-22 |	17:08:00 |	Rufus |	Does that did before did not fill this now
5 | 2021-08-22 |    17:08:00 |	Goodness CSC |	Just fill the part I aspect
