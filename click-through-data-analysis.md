# Project objective and scope

The scope of this project is to create an analytics report that summarizes the click-through data collected by Hospice Palliative Care, Ontario (HPCO) from its Newsletter Subscribers. The results of this analysis will help HPCO decide on the right marketing strategy to drive up subscriptions as well as subscriber engagement with their publications.

The raw data was obtained from HPCO constant contact data, which needed further specialized attention, breaking down the numbers, to obtain data that excluded HPCO employees, who were also subscribers to the Newsletter.

## Understanding the Project problem and deliverables

The first phase of the project consisted of getting a theoretical overview of Marketing Data Analytics, which is a subset of Digital Marketing. Also, I needed to get a good grasp of the domain context of the problem.

The problem centered around the effectiveness of the bi-weekly newsletter content being put out by HPCO. The goal was to find out any underlying trends in the newsletter content that seems to be more appealing to the newsletter subscribers to click on.

The content of this newsletter is target-specific, directed to those within the Hospice Care community and other stakeholders in that sector. The newsletter is a mass communication tool that featured various kinds of content, which includes upcoming webinars and events, product, and service updates, calls for participation on committees, job postings, research articles, amongst other things. Each item includes a link that leads to more information elaborating on the content in the newsletter.

Another challenge that needed to be solved was the filtering out of HPCO employees from the data, as this analysis is targeted at external stakeholders. That was not practically an easy thing to do, based on the initial format and nature of the data.

To wrap up this section, the goal was to identify any insight that will lead to HPCO developing more appealing content for its newsletter subscribers. It took me a total of 12 hours of research and study to gain a good grasp of the problem, and to devise a workable approach in creating an effective solution.

## Understanding the Data

The next phase of the project involved getting more familiar with the data. The data was received as an Excel file containing several worksheets, which represented the click-through data. Each edition of the Newsletter Data contained subscriber information, such as names, email addresses, Company, Job title, contact sources, Email lists, as well as other metadata that were not directly used in the analysis.

Also included in the Excel workbook was a summary worksheet that showed a summary of each edition’s sends, opens, open rates, click rates and bounce rates. This summary as well as the detailed data included those belonging to HPCO employees.
It took me about 8 hours to complete this phase.

## Creation of Visuals in Power BI

This phase was the longest phase of the project, where I undertook the task of creating a dashboard and replicating it 27 times for each Newsletter Edition. It took me some time (5 hours) to settle on the optimal approach in summarizing the data, filtering out unwanted data points, and transforming the data into a workable model.

I also created a visual showing the click-through summary data with the HPCO employees filtered out. I was able to use Power BI capabilities to implement the filtering and allow the data show only non-HPCO employees. Below is a screenshot of the summary table visual:

![image](https://github.com/ovokpus/my-bi-gallery/blob/main/images/hpco-click-through-summary.png)

---

The subsequent slides of this visual report contained the 27 dashboards, showing click-through data for each edition of the newsletter from June 10, 2020, to June 9, 2021.

On the top half of each dashboard, we have a list of the Top Clicked link addresses shown in a horizontal bar chart. The numbers beside each bar represent the number of distinct users who clicked on those links. For example, on June 10, 2020, 25 unique users clicked on the topmost link with the longest bar.
At the bottom left of the report is a table showing the clicked link addresses, along with the number of times those links were clicked (shown in the Total Column). This number is also further broken down into the various contact sources. At the bottom right is a donut chart that shows a spread of the number of clinked links by the day of the month on which the Newsletter Edition was released.

Below are a sampling of screenshots showing different dashboards I created. The other piece of this reporting then included the creation of detailed results from the top 5 most clicked links from each edition. This process involved identifying the location of each link in the original newsletter edition, to identify what content that link was mapped with. This was a slow and painstaking process which took me another 25 hours to complete.

![image](https://github.com/ovokpus/my-bi-gallery/blob/main/images/hpco-july-2020.png)

---

![image](https://github.com/ovokpus/my-bi-gallery/blob/main/images/hpco-june-2021.png)

---

![image](https://github.com/ovokpus/my-bi-gallery/blob/main/images/hpco-march-2021.png)

---

![image](https://github.com/ovokpus/my-bi-gallery/blob/main/images/hpco-oct-2020.png)

---

Sample Report of 5 most clicked links per edition
![image](https://github.com/ovokpus/my-bi-gallery/blob/main/images/hpco-sample-summary-report.png)

---

# Summarizing the Report

The report summary included information regarding the top 3 and bottom 3 most clicked links, as well as the following findings:

1. The contact source data shows that Webinar had the most clicks, followed by NL
2. A huge percentage of the clicks were made within a day or two from the release date of each edition
3. Of the top 5 most clicked links from each edition, the highest number of clicks were made on Job Postings (38), followed by Events and Webinars (24)
4. On the two occasions where the links clicked led to a web page with video content, those links ended up the most clicked links for those editions (December 9 and December 23, 2020)
5. There is apparently no correlation between the position of the article on the Newsletter and the number of clicks. However, that correlation seems to appear when we filter out the Job postings. Articles appearing at the top, or near the top of the web page had more clicks.
6. No established correlation between an article having image content and number of clicks.
