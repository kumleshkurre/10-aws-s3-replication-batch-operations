# 📦 AWS S3 Bucket Replication & Batch Operations Guide

### 📌 Overview
---

#### This guide explains how to:
- Create an Amazon S3 bucket
- Configure S3 Replication Rules
- Use S3 Batch Operations
- Automatically replicate objects from a source bucket to a destination bucket
---

## 🪣 Step 1: Create an S3 Bucket
- Open AWS Management Console
- Go to S3 → Create bucket
- Select: Bucket type: General purpose
- Bucket name: Choose a unique name (example: kurrebucket711)
- Click Create bucket
---

## 🔁 Step 2: Configure S3 Replication Rule
-  Open Source Bucket
- Go to S3
- Open the source bucket
- Navigate to the Management tab

#### Create Replication Rule
- Click Create replication rule
- Configure the rule:
- Rule name: kurrebucket-replication-rule
- Status: Enabled
- Rule scope: Apply to all objects in the bucket
- Destination settings:
- Destination: Choose a bucket in this account
- Click Browse S3
- Select destination bucket (example: kalibucket711)
- IAM Role:
- Select Create new IAM role
- Click Save
- Enable: ☑ Yes, replicate existing objects
- Click Submit
---

## ⚙️ Step 3: Create S3 Batch Operations Job
### Step 1. Job Execution Settings
- Choose: Automatically run the job when it’s ready
- IAM Role: Select Create new IAM role
- Click Save
---

### Step 2. Object List & Destination
#### Object list configuration:
- Choose Generate an object list by specifying filters
- Source account & bucket:
- Source bucket: kurrebucket711
- Click Next

#### Destination bucket:
- Select destination bucket (example: kalibucket711)

#### Permissions:
- Choose Create new IAM role
- Review
- Click Create and Submit
---

## ✅ Step 4: Verify Replication
- Go to the source bucket
- Upload a new file
- The file will be automatically replicated to the destination bucket
---

## 📝 Important Notes
- ✅ Replication rule must be enabled, otherwise replication will not work
- 🔐 IAM roles are mandatory for replication and batch operations
- 🔄 Both existing and new objects can be replicated
---

## 🎯 Use Case
- Cross-bucket backup
- Disaster recovery
- Data synchronization
- Compliance and auditing
---

## 📚 References
- Amazon S3 Replication
- Amazon S3 Batch Operations
- AWS IAM Roles
---

  ## 👨‍💻 Author

**Kumlesh Kurre**
💼 IT Support & Network Engineer

⭐ If you find this guide helpful, don’t forget to star ⭐ the GitHub repository!
