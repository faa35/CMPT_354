


## Setup Instructions
If file size greater than 100mb it will casue problem.  
```
File HW/HW_4/flight.db is 152.93 MB; this exceeds GitHub's file size limit of 100.00 MB
```   
For that, we are gonna upload it with Git LFS

1. **Initialize Git and Git LFS:**
   - Installed Git LFS on Windows from [here](https://git-lfs.github.com/).
   - Initialized Git and tracked `flight.db` with Git LFS:
     ```bash
     git lfs install
     git lfs track "HW/HW_4/flight.db"
     ```

2. **Add and Commit Files:**
   - Added files: `flight.db` (large file) and `hw4.ipynb`.
   ```bash
   git add .
   git commit -m "Added files & track large file with LFS"
   ```

3. **Push to GitHub:**
   - Pushed changes to the remote repository:
   ```bash
   git push origin main
   ```

Git LFS handles uploading the large file separately to stay within GitHub's file size limits.
