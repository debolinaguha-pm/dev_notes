📘 Guide: How to Push Code from Local VS Code to GitHub (Mac, HTTPS)
🔧 Step 1: Initialize Git in your project
Open terminal inside your project folder and run:

bash
Copy
Edit
git init
(If already initialized, you’ll see: Reinitialized existing Git repository)

📝 Step 2: Create a README file (optional)
bash
Copy
Edit
echo "# your-project-name" >> README.md
🗃️ Step 3: Add and commit your files
bash
Copy
Edit
git add .
git commit -m "Initial commit"
🌿 Step 4: Create the main branch (if needed)
bash
Copy
Edit
git branch -M main
🔑 Step 5: Generate a GitHub Personal Access Token (HTTPS method)
Go to: https://github.com/settings/tokens?type=beta

Click Generate new token

Give it a name (e.g. "VS Code Push Token")

Set expiration (e.g. 90 days or custom)

Check ✅ repo under scopes

Click Generate token

Copy the token (you’ll use it only once in the terminal)

🔗 Step 6: Connect your local repo to GitHub using the token
Replace YOUR_TOKEN with the token you just copied:

bash
Copy
Edit
git remote add origin https://your-github-username:YOUR_TOKEN@github.com/your-github-username/your-repo-name.git
Example:

bash
Copy
Edit
git remote add origin https://debolinaguha-pm:ghp_xxxTOKENxxx@github.com/debolinaguha-pm/ultimate-html-css-portfolio.git
🚀 Step 7: Push your code
bash
Copy
Edit
git push -u origin main
✅ This should now succeed and push your code to GitHub.

🧹 Optional Cleanup (remove token from visible remote)
Once the push works, reset the remote to the clean format:

bash
Copy
Edit
git remote set-url origin https://github.com/your-github-username/your-repo-name.git