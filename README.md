# Netflix-Analytics-AWS-Cloud-Project

This repository contains my personal project and learning experience with AWS Cloud. Over a series of steps, I created a stunning dashboard of graphs and visualizations using Amazon QuickSight. Below is a step-by-step guide on how I achieved this.

---

## Table of Contents

- [Step #1: Download the Dataset](#step-1-download-the-dataset)
- [Step #2: Store the Dataset in Amazon S3](#step-2-store-the-dataset-in-amazon-s3)
- [Step #3: Amazon QuickSight Account](#step-3-create-amazon-quicksight-account)
- [Step #4: S3 Bucket to Amazon QuickSight](#step-4-connect-s3-bucket-to-amazon-quicksight)
- [Step #5: QuickSight Visualization](#step-5-create-quicksight-visualization)
- [Step #6: Final results](#step-7-final-results)
- [Cleanup](#cleanup)
- [Conclusion](#conclusion)

---

## Step #1: Download the Dataset

Download the required files:
- [netflix_titles.csv](https://github.com/DaudCloud-sudo/Netflix-Analytics-AWS-Cloud-Project/blob/main/netflix_titles.csv) 
- [manifest.json](https://github.com/DaudCloud-sudo/Netflix-Analytics-AWS-Cloud-Project/blob/main/manifest.json) 

---

## Step #2: Store the Dataset in Amazon S3

1. Log in to your AWS Account.
2. Open your **S3** service.
3. Create a new bucket:
    - Name the bucket: `your-name-netflix-data`
    - Select the region closest to you.
    - Keep the rest of the settings as default, and create the bucket.

4. Upload the CSV file and the JSON file into the bucket.
5. Copy the S3 URL of your CSV file.
6. Open the manifest.json file in your text editor.
7. Replace the URL in the manifest.json file with the S3 URL of your CSV dataset.
8. Re-upload the edited manifest.json file into your bucket, which will automatically replace the existing one.

### Screenshot of S3 Bucket
![S3 Bucket Screenshot](path_to_screenshot)

---

## Step #3: Create Your Amazon QuickSight Account

1. Search for **QuickSight** in the AWS Management Console.
2. Sign up for the free QuickSight trial (Standard edition).
3. Uncheck the "Add Paginated Reports" option.
4. Enter your details for your QuickSight account.
5. Select **Finish**.

### Screenshot of QuickSight Success Page
![QuickSight Success](path_to_screenshot)

---

## Step #4: Connect Your S3 Bucket to Amazon QuickSight

1. From the QuickSight home page, go to **Manage Data** > **New Data Set**.
2. Select **S3**.
3. For the first field (source name), enter `netflix_titles_kaggle`.
4. Enter the S3 URL to your manifest.json file.
5. Select **Connect**.
6. Select **Visualize**.

### Screenshot of S3 Connection Setup
![S3 Connection Setup](path_to_screenshot)

---

## Step #5: Create Your First QuickSight Visualization

1. Drag `release_year` into the Y-Axis heading.
2. Change the chart type to a donut chart.

### Screenshot of First Visualization
![First Visualization](path_to_screenshot)

---

## Step #6: QuickSight Treasure Hunt

1. **Task 1:** Create a stacked bar chart to visualize the percentage of TV shows and movies for each release year.
    - Change the graph type to a Horizontal stacked 100% bar chart.

2. **Task 2:** Create a table showing the number of movies vs TV shows per release year.
    - Change the visual type to Table, then add `release_year` as the Group By label, `title` as the Value metric, and `type` as a dimension.

3. **Task 3:** Find the day Netflix added the largest number of movies/TV shows to their catalog.
    - Move the `date_added` label to both the Y Axis and Value headings. Sort by descending to find the largest number.

4. **Task 4:** Count how many titles are listed as 'Action & Adventure', 'TV Comedies', or 'Thrillers'.
    - Add a filter for the `listed_in` field and select these three tags.

5. **Task 5:** Of the titles listed in Task 4, count how many were released on or after 2015.
    - Apply a filter for `release_year` and select 2015 and later.

### Screenshot of Visualization with Filters
![Filtered Visualization](path_to_screenshot)

---

## Step #7: Finishing Touches

1. Edit the titles of your charts for clarity.
2. Publish your dashboard.
3. Export your dashboard as a PDF.

### Screenshot of Final Dashboard
![Final Dashboard](path_to_screenshot)

---

![My Dashboard](../mnt/data/image.png)

---

## Cleanup

1. Terminate your QuickSight account:
    - Go to **Manage QuickSight** > **Account Settings**.
    - Toggle off account termination and type "delete account".
    
2. Delete your S3 bucket:
    - Empty the bucket first, then delete it.

---

## Conclusion

In this project, I successfully created a dashboard using Amazon QuickSight by:
- Uploading a dataset into an S3 bucket.
- Connecting the dataset to QuickSight.
- Creating various visualizations.
- Experimenting with different visualization styles.
- Forming a comprehensive dashboard and exporting it.

This hands-on experience with AWS services and QuickSight was both challenging and rewarding, enhancing my skills in cloud-based data visualization.

