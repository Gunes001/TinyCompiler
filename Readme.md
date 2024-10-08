This is a Tiny Compile in Swift to show the basic principle of compiler technology.



The error message indicates you're trying to push to GitHub using a password, but password authentication for Git operations was removed on August 13, 2021. Here's how to fix it:

**Solution: Use a Personal Access Token (PAT) instead of password**

1. **Generate a Personal Access Token:**

   - Log in to your GitHub account.
   - Go to **Settings** (click on your profile picture in the top right corner).
   - Navigate to **Developer settings** in the sidebar.
   - Click on **Personal access tokens**.
   - Click on **Generate new token**.
   - Give your token a descriptive name (e.g., "TinyCompiler Push").
   - Select the scopes your token needs (usually "repo").
   - Click on **Generate token**.
   - Copy the generated token (it won't be displayed again).

2. **Update your Git remote URL:**

   - Open your terminal and navigate to your project directory.

   - If you haven't already, clone the repository using HTTPS:

     Bash

     ```
     git clone https://<your_username>@github.com/<your_username>/TinyCompiler.git
     ```

     请[谨慎使用]()代码。

   - If you cloned using SSH before, update the remote URL:

     Bash

     ```
     git remote set-url origin https://<your_access_token>@github.com/Gunes001/TinyCompiler.git
     ```

     请[谨慎使用]()代码。

     Replace `<your_access_token>` with the actual token you generated in step 1.

3. **Push your changes:**

   Bash

   ```
   git push origin main
   ```