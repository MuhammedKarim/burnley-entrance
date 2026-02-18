# 📿 Masjid Prayer Timetable Display

🔴 **Live Status Website:** [https://muhammedkarim.github.io/burnley-entrance](https://muhammedkarim.github.io/burnley-entrance)  
(Click to view the live display being used in the masjid.)

---

## 🙏 How to Make Changes

These instructions will help you:
1. ✏️ Edit a specific **prayer time**
2. 🖼️ **Add or remove** posters (images)
3. 🔄 Update `version.json` to **push your changes live Immediately**

You can do this **from the GitHub website** on your **computer or phone**.

---

### 1️⃣ How to Change a Prayer Time

For example, you want to change **Dhuhr Jamat time on June 15th**.

#### Steps:
1. Go to the file: [`prayer-times.json`](./prayer-times.json)
2. Click the **pencil icon** ✏️ in the top right to edit.
3. Find the date, e.g. `"2025-06-15"` (Use Ctrl+F or "Find" to search).
4. You will see something like:
   ```jsonc
   "2025-06-15": { ... "dhuhr": { "start": "13:06", "jamat": "13:30" }, ... }
   ```
5. Edit the **"jamat"** value as needed. For example:
   ```json
   "jamat": "13:15"
   ```
6. Click **“Commit changes”**, then confirm by clicking the green button again.

---

### 2️⃣ How to Add or Remove Posters

These are full-screen images that display between prayer times.

#### 🖼️ Naming Rules:
- Posters must be placed in the **`posters/` folder**.
- Name them as: `1.jpg`, `2.jpg`, `3.jpg`, `4.jpg`, `5.jpg`
- You can have up to **5 images** at once.
- **They will display in order**, each for 10 seconds.

#### ➕ To Add a Poster:
1. Go to the [`posters/`](./posters) folder.
2. Click **“Add file” → “Upload files”**.
3. Upload your JPG file.
4. Rename it (if needed) to `1.jpg`, `2.jpg`, etc. to follow the numbering.
5. Click **“Commit changes”**.

#### ➖ To Remove a Poster:
1. Open the [`posters/`](./posters) folder.
2. Click the file you want to delete (e.g. `3.jpg`).
3. Click the three dots at the top-right corner of the file preview.
4. Choose **"Delete file"**.
5. Confirm by clicking **“Commit changes”**.

---

### 3️⃣ How to Push Changes Live Immediately

Any time you:
- Edit `prayer-times.json`
- Add/remove posters

The system will automatically update **within 5 minutes**, even if you don’t do anything else.

However, if the update is **urgent** and you want it to appear on the live screen **within a minute**, you should also update the `version.json` file to force a refresh.

#### Steps to Trigger Immediate Refresh:
1. Open [`version.json`](./version.json)
2. Click the **pencil icon** ✏️
3. Change the version from `"1"` to `"2"`, or from `"2"` to `"1"` (just switch between them).
   
   Example:
   ```json
   { "version": "2" }
   ```
4. Click **“Commit changes”**.

That’s it! The screen at the masjid will detect the version change and automatically reload to apply your updates almost immediately.
