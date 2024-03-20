# How to connect MadCap Flare to GitHub Pages

> [!CAUTION]
> Make sure that you arleady have installed Git on your computer. 
>
> If not, you can use this [LINK](https://git-scm.com/downloads) to download.

## Step 1. Connect your MadCap Flare project to the GitHub repository

1. Create a new GitHub repository.

![View of creating a new repository in GitHub](./Resources/Create-a-new-GitHub-repository.png)

2. Copy the link to your new repository.

![View of the link to the new GitHub repository](./Resources/Copy-the-link-to-your-new-repository.png)

3. In your MadCap Flare, click **Project** > **Project Properties** > **Source Control** > **Bind Project**.

![View of how to bind project in MadCap Flare](./Resources/Bind-project.png)

4. Choose **Git** as your Source Control Provider.
5. Choose the **Remote Repository** checkbox.
6. Choose the **Push on bind** checkbox.
7. Paste the link to your repository.
8. Enter your name, email address and click **OK**.

![View of how to bind project in MadCap Flare - next step](./Resources/Bind-project-next-step.png)

>[!NOTE]
> MadCap Flare may ask you to enter your GitHub login and password here. When such a dialog box appears, provide these data.

9. Go to your GitHub repository and refresh the page to see the changes.

![Project uploaded to GitHub view](./Resources/Project-uploaded-to-GitHub-view.png)

Your local project has been uploaded to your GitHub repository.

## Step 2. Project preparing for publication on GitHub Pages

1. In your MadCap Flare, click **Project Organizer** > **Targets** > **HTML5** > **General** and change 'home.htm' to 'index.html' in **Output File** section.

![Change the output file in MadCap Flare](./Resources/Change-the-output-file.png)

Save changes.

2. Create a new Publishing Destination using **Project Organizer** > **Targets** > **HTML5** > **Publishing** > **New Destination...** and clicking **Add**.

![Create a new publishing destinaton in MadCap Flare](./Resources/Publishing-destination.png)

3. Create a target folder "Docs" in your local project. It should be in the main directory of the project that we bind with Git.

![Create a target folder](./Resources/Target-folder.png) 

> [!CAUTION]
> The name of the target folder is case-sensitive.
> 
> Example: if you named the folder "Docs" - enter the name in capital letter. If you used "docs", then enter lowercase letters.

4. Choose Source Control type and provide the target folder destination.

![Create a new files destination](./Resources/New-destination.png)

Save your work.

5. Go back to the **Project Organizer** > **Targets** > **HTML5** > **Publishing** menu and select **Publish** checkbox.

Save changes and click **Publish**.

![Publish settings view](./Resources/Publish.png)

The output with your completed website should jump into the folder you just selected (in my case: "Docs").

>[!NOTE]
> From now on, in the "Source Control" menu (at the top, in the taskbar), you will find standard Git operations - commit, pull and push.
> 
> Now you can change the local files in your MadCap project, commit the changes and push them to the remote repository.

![View of Git operations in MadCap Flare taskbar](./Resources/Source-control.png)

## Step 3. Project publication

Select **Project** > **Publish Primary** > **Publish "HTML5"**

![Gif with publishing steps](./Resources/Publish-primary-HTML5.gif)

Now the entire project should be uploaded to your GitHub repository.

## Step 4. Publish as GitHub Pages

1. Open your GitHub repository settings.
Select **Pages** and set **GitHub Actions** as a GitHub Pages source.

![View of GitHub Pages settings](./Resources/GitHub-Pages-settings.png)

1. Select **Actions** section and click **New workflow**.

![Click "new workflow" button](./Resources/New-workflow.png)

3. Search for **static** in **Search workflows** and click **Configure** for **Static HTML**.

![Configuration of Static HTML workflow](./Resources/Static-workflow.png)

4. Change path from '.' to 'Docs' and click **Commit changes...**.

> [!CAUTION]
> Remember that the name of the target folder is case-sensitive.

![Configuration of static.yml file](./Resources/Static-yml-file-configuration.gif)

5. Select **Actions** section and click **Deploy static content to Pages**.
Click **Run workflow** for branch: master.

![View how to run workflow](./Resources/Run-workflow.png)

...and YOU GOT IT! Congratulations! 🎉

Now you can go to **Deployments** in your GitHub repository and admire your website implemented directly from MadCap Flare to GitHub Pages! 🚀

### Kindly reminder
Just remember that whenever you make changes in the MadCap Flare project that you want to publish to the website - repeat step 3, publishing the HTML5 result. 

![Gif with publishing steps](./Resources/Publish-primary-HTML5.gif)

**ENJOY!** 😊

### Sources
- [DocWizard/GHPages-howto](https://github.com/DocWizard/GHPages-howto)
- [Documentation Portal: How to connect MadCap Flare to Git](https://docsy-site.netlify.app/docs/madcap-flare/connect-madcap-to-git/#bind-using-the-flare-interface)