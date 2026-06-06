# Exam Submission Portal — Setup Guide

## Step 1 — Get your Uploadcare Public Key (free, 2 mins)

1. Go to https://uploadcare.com and create a free account
2. After signing in, go to your **Dashboard**
3. Click on your project (or create one called "ExamPortal")
4. Copy your **Public Key** (looks like: `demopublickey`)

## Step 2 — Add your key to the HTML file

Open `index.html` and find this line near the bottom:

```js
const UPLOADCARE_PUBLIC_KEY = 'YOUR_PUBLIC_KEY_HERE';
```

Replace `YOUR_PUBLIC_KEY_HERE` with your actual key. Save the file.

## Step 3 — Deploy to Vercel (free, 2 mins)

### Option A — Drag & Drop (easiest)
1. Go to https://vercel.com and sign in (or create a free account)
2. From your dashboard, click **Add New → Project**
3. Choose **"Deploy without a Git repository"** (or drag the folder)
4. Drag the entire `exam-submission` folder into the upload area
5. Click **Deploy**
6. Vercel gives you a URL like: `https://exam-submission-xyz.vercel.app`

### Option B — Vercel CLI
```bash
npm i -g vercel
cd exam-submission
vercel --prod
```

## Step 4 — Share the URL with students

Send students the Vercel URL. They:
1. Enter their full name
2. Select and upload their files
3. Hit Submit — done!

## Step 5 — View Submissions

1. Log into https://uploadcare.com
2. Go to **Files** in the dashboard
3. All files are named with the format: `YYYY-MM-DD__Student_Name__filename.ext`
4. Filter or search by student name
5. Select all and download as a ZIP

## Notes

- Free Uploadcare plan: 3GB storage, 30GB bandwidth/month — more than enough for 30 students
- Files are stored permanently until you delete them
- No student can see another student's files
- The portal can be reused for future exams (just clear old files from Uploadcare)
