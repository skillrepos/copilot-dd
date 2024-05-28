# Copilot Deep Dive - lab setup

These instructions will guide you through configuring a GitHub Codespaces environment that you can use to run the course labs. 
If you prefer and if you know one of the other IDEs supported by Copilot, you can use that. But the instructions will reference the codespace version.

These steps **must** be completed prior to starting the actual labs.

## 1. Ensure that you are signed up for Copilot access. 

If not, when signed into GitHub, click on your profile picture/icon in the upper right and either select [Copilot](https://github.com/github-copilot/signup) 

![Signing up for Copilot](./images/cdd70.png?raw=true "Signing up for Copilot")

**OR** select [Settings->Copilot](https://github.com/settings/copilot) and sign up.

![Signing up for Copilot](./images/cdd32.png?raw=true "Signing up for Copilot")

You can also find help there for using Copilot in other supported IDEs, set the switch for whether or not to allow matching public code suggestions, etc.

![Using Copilot options](./images/cdd31.png?raw=true "Using Copilot options")
<br/><br/>
## 2. From here you **may use either of the options below:**
<br/><br/>
## Option 1 - _Use if you just want a quick start without a fork of the repo_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Create a codespace without a repository to commit to by clicking on the button below:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/skillrepos/copilot-dd?quickstart=1)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Then click on the option to create a new workspace.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Creating new codespace from button](./images/cdd109.png?raw=true "Creating new codespace from button")

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**This will run for several minutes while it gets everything ready.**
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- After the codespace has initialized there will be a terminal present.

<br/><br/>

## Option 2 - _Use if you want a forked copy of the repository to update with your changes_


### a. Create your own fork of the repository for these labs

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Ensure that you have created a repository by forking the [skillrepos/copilot-dd](https://github.com/skillrepos/copilot-dd) project as a template into your own GitHub area.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- You do this by navigating to the repo, clicking the `Fork` button in the upper right portion of the main project page and following the steps to create a copy in **your-github-userid/copilot-dd** .

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Forking repository](./images/cdd28.png?raw=true "Forking the repository")
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Forking repository](./images/cdd29.png?raw=true "Forking the repository")

### b. Configure your codespace

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In your forked repository, start a new codespace.


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Click the `Code` button on your repository's landing page.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Click the `Codespaces` tab.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Click `Create codespaces on main` to create the codespace.

**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This will run for several minutes while it gets everything ready.**
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- After the codespace has initialized there will be a terminal present.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Starting codespace](./images/cdd30.png?raw=true "Starting your codespace")

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This will take a while to run.
<br/><br/>
## 3. Open the labs

After the codespace has started, open the labs document by going to the file tree on the left, find the file named **codespace-labs.md**, right-click on it, and open it with the **Preview** option.)

![Labs doc preview in codespace](./images/cdd33.png?raw=true "Labs doc preview in codespace")

This will open it up in a tab above your terminal. Then you can follow along with the steps in the labs. 
Any command in the gray boxes is either code intended to be run in the console or code to be updated in a file.

Labs doc: [Copilot Deep Dive Labs](codespace-labs.md)


