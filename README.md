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
    - Name the bucket.
    - Select the region closest to you.
    - Keep the rest of the settings as default, and create the bucket.
  
![image](https://github.com/user-attachments/assets/c477157a-666d-47e1-8874-c87880c91421)

4. Upload the CSV file and the JSON file into the bucket.
5. Copy the S3 URL of your CSV file.
6. Open the manifest.json file in your text editor.

![image](https://github.com/user-attachments/assets/b6b7cb27-702f-4071-9ce9-dbd476caed64)

8. Replace the URL in the manifest.json file with the S3 URL of your CSV dataset.
9. Re-upload the edited manifest.json file into your bucket, which will automatically replace the existing one.

![image](https://github.com/user-attachments/assets/f56bed41-086c-40a2-beb8-2e53e81a1227)

---

## Step #3: Create Your Amazon QuickSight Account

1. Search for **QuickSight** in the AWS Management Console.
2. Sign up for the free QuickSight trial (Standard edition).
3. Uncheck the "Add Paginated Reports" option.
4. Enter your details for your QuickSight account.
5. Select **Finish**.

![image](https://github.com/user-attachments/assets/cf67e0dc-86d0-47ad-aed8-f60125838fd1)

---

## Step #4: Connect Your S3 Bucket to Amazon QuickSight

1. From the QuickSight home page, go to **Manage Data** > **New Data Set**.
2. Select **S3**.
3. For the first field (source name), enter `netflix_titles_kaggle`.
4. Enter the S3 URL to your manifest.json file.
5. Select **Connect**.
6. Select **Visualize**.

![image](https://github.com/user-attachments/assets/fb0a1c09-5447-4029-b3d3-f4f4c2e8e207)
![image](https://github.com/user-attachments/assets/a84f32f0-195d-485e-9b6f-641707f1599f)

---

## Step #5: Create QuickSight Visualization

1. Drag `release_year` into the Y-Axis heading.
2. Change the chart type to a don
### Screenshot of First Visualization
![First Visualization](path_to_screenshot)

---

## Step #7: Finial Result

![image](https://github.com/user-attachments/assets/c85323e5-393a-4433-a448-e7e52ced599e)

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

