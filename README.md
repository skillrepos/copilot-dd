# Copilot Deep Dive - lab setup

These instructions will guide you through configuring a GitHub Codespaces environment that you can use to run the course labs. 
If you prefer and if you know one of the other IDEs supported by Copilot, you can use that. But the instructions will reference the codespace version.

**NOTES:**
1. We will be working in the public GitHub.com, not a private instance.
2. Chrome may work better than Firefox for some tasks.
3. The default environment will be a GitHub Codespace (with Copilot already installed). If you prefer to use your own IDE, you are responsible for installing Copilot in it. Some things in the lab may be different if you use your own environment.
4. To copy and paste in the codespace, you may need to use keyboard commands - CTRL-C and CTRL-V.
5. VPNs may interfere with the ability to run the codespace. It is recommended to not use a VPN if you run into problems.
6. If you use the new free Copilot plan (no signup), some advanced functionality may not be available. Pro version is free trial for 30 days.
</br></br></br>

These steps **must** be completed prior to starting the actual labs.

## 1. When logged into GitHub, you have Copilot Free version. This will let you do almost everything in the class. (If you prefer, you can sign up for the Pro version trial to be able to do all steps, but that is not required.)

Only if you want to sign up for the Pro trial, click on your profile picture/icon in the upper right and select [Your Copilot](https://github.com/github-copilot/signup), **OR** select [Settings->Copilot](https://github.com/settings/copilot). Then click on *Start a free trial*. 

![Signing up for Copilot](./images/cdd201.png?raw=true "Signing up for Copilot")
![Signing up for Copilot](./images/cdd202.png?raw=true "Signing up for Copilot")

You can also find help there for using Copilot in other supported IDEs, set the switch for whether or not to allow matching public code suggestions, etc.

![Using Copilot options](./images/cdd31.png?raw=true "Using Copilot options")
<br/><br/>
## 2. Create your own codespace to run the labs by clicking on the button below.
<br/><br/>

Click here ------> [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/skillrepos/copilot-dd?quickstart=1)

<br/><br/>

Then click on the option to create a new codespace.

![Creating new codespace from button](./images/cdd109.png?raw=true "Creating new codespace from button")

**This will run for several minutes while it gets everything ready.**

<br/><br/>

## 3. Open the labs

After the codespace has started, open the labs document by going to the file tree on the left, find the file named **codespace-labs.md**, right-click on it, and open it with the **Preview** option.) *Alternatively, you can open it up in a separate browser tab directly from the GitHub site.*

![Labs doc preview in codespace](./images/cdd33.png?raw=true "Labs doc preview in codespace")

This will open it up in a tab above your terminal. Then you can follow along with the steps in the labs. 
Any command in the gray boxes is either code intended to be run in the console or code to be updated in a file.

Labs doc: [Copilot Deep Dive Labs](codespace-labs.md)

<br/><br/>

## 4. Set codespace timeout (optional but recommended)

While logged in to GitHub, go to [https://github.com/settings/codespaces](https://github.com/settings/codespaces).

Scroll down and find the section on the page labeled *Default idle timeout*. 

Increase the default timeout value to 90 minutes and then select the *Save* button.

![Increasing default timeout](./images/cdd200.png?raw=true "Increasing default timeout")

(**NOTE**: If your codespace does time out at some point in the course, there should be a button to restart it.)

