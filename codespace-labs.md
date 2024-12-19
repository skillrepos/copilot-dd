# Copilot Deep Dive
## An introduction to GitHub Copilot
## Session labs for codespace only
## Revision 6.2 - 12/19/24

**Versions of dialogs, buttons, etc. shown in screenshots may differ from current version of Copilot**

**Follow the startup instructions in the README.md file IF NOT ALREADY DONE!**

**NOTES:**
1. Chrome may work better than Firefox for some tasks.
2. To copy and paste in the codespace, you may need to use keyboard commands - CTRL-C and CTRL-V.**
3. VPNs may interfere with the ability to run the codespace. It is recommended to not use a VPN if you run into problems.
4. If you use the new free Copilot plan (no signup), some advanced functionality may not be available.
</br></br></br>
   

**Lab 1 - Learning how to create good prompts for Copilot**

**Purpose: In this lab, we’ll start to learn about Copilot and how it generates code based on the prompts we provide**

1. Create a new file. In the terminal, enter

   ```
   code index.js
   ```
   
![Creating file from terminal](./images/cdd173.png?raw=true "Creating file from terminal")

2. Afterwards this file should be open in a tab in the editor.

3. Let's see how Copilot responds to a generic request. Go to that tab and type in a comment that says

```
// function to parse data
```
4. Hit return and notice the code that Copilot suggested. This is likely more generic than we want, but hit tab to select that line. (Note that you should give Copilot a second to provide code suggestions before moving on to the next line.)
   
5. After hitting tab, Copilot will generate another part of the function. (If not, you may need to hit return.) Hit tab to accept it. Continue until you get a complete function (or Copilot stops generating additional code suggestions). One example of what code may look like is below. (This likely won't be the same as yours.)

![Copilot generated function](./images/cdd2.png?raw=true "Copilot generated function")
   
6. This prompt is not specific enough for Copilot to interpret what we want to do.  Highlight the code and delete it, so we can try again.

7. Now type a comment at the top that says

```
// function to parse url
```
8. Hit enter and you will probably see a similar line to

```
function parseURL(url) {
```

9. Just hit Tab to accept it and Enter again. Pause. After that Copilot may or may not offer a suggestion.  If it does, great - you can just hit Tab and accept it.  If not, it may be necessary to further "nudge" Copilot by giving more prompts. Only if you're not getting responses from Copilot, hit return and type the comment below to nudge Copilot.

```
// parse url
```
![nudge comment](./images/cdd3.png?raw=true "nudge comment")   

10. Only if needed, hit return and Copilot should start generating suggestions again. Pause after each return to give Copilot a chance to suggest code. Then you can just hit tab to accept each line and then return to get the next part of the code until the function is complete. You may get some blank lines along the way or for some lines you might need to hit Tab twice to accept the code if it is indented more. But just hit return until you get to the end of a function. (You will be at the end when the indentation is done.  Also Copilot may start to suggest another function in comments like // test...)

11. Suppose you're not happy with that suggestion. Copilot can provide other options for the code. To see those, make sure you are in the editor for the file, then delete all but the first line of the function **and** put the cursor at the end of the first line.

![reset for altenate choices](./images/cdd105.png?raw=true "reset for alternate choices")   
   
12. Hit **Ctrl + Enter**. A second window will open up with other suggestions.
Be patient - it takes a bit of time for Copilot to generate alternative suggestions. After a moment though, you will have up to 10 alternatives to pick from. These will be of varying quality and completeness. You can scan through these and then pick one if suitable by clicking on the **Accept suggestion #** button under the alternative suggestion.  Note that this will add the code to the existing set, so you may need to do some minor editing afterwards.

![alternative suggestions](./images/cdd106.png?raw=true "alternative suggestions")   

13. Let's do one more pass at getting a specific prompt for Copilot. Delete all the code currently in index.js. This time we will not enter a comment, but will enter a specific function name.
Type the following in the empty file. (There are no parentheses after the *splitURLandReturnComponents* text.)  Do not hit tab or return yet.

```
function splitURLandReturnComponents
```

14.  With this function name, Copilot should suggest a full function definition - in fact it may suggest several.  To see the options, hover over the first line and a small window should appear. This window will not how many options there are (probably 2 or 3) and provide "<" and ">" links to toggle between them.  Click on the "<" and ">" buttons to see the differences in the available suggestions.

![alternative suggestions inline](./images/cdd5b.png?raw=true "alternative suggestions inline")   

15. When you find an alternative you like, go ahead and tab to select it.

 <p align="center">
**[END OF LAB]**
</p>
</br></br></br>

**Lab 2 - Using Copilot to simplify code**

1. Create a new file named prime.py. Create it via the same process as we used in Lab 1 by entering the line below in the terminal.

```
code prime.py
```

2. In the new editor tab for the file, start typing a function definition as below
```
def is_prime(n):
```
3. Leave the cursor at the end of the line.

![starting point](./images/cdd104.png?raw=true "starting point") 

4. Hit **Ctrl+Enter** to see options

5. Pick one of the options that is longer and/or more complex (if there is one) and **Accept suggestion #**. If there's not one that's longer/more complex, just pick an alternative one and **Accept suggestion #**.

![alternative suggestions](./images/cdd34b.png?raw=true "alternative suggestions") 

6. Highlight the code and select the Chat extension icon to open the chat window.  Tell Copilot to simplify the code by typing in the chat window.
```
simplify
```

![simplifying via chat box](./images/cdd174.png?raw=true "simplifying via chat box") 

7. Hover over the simplified text and tell Copilot to insert the suggestion at the cursor to replace the text that's currently there. Accept any changes.

![replace from chat suggestion](./images/cdd175.png?raw=true "replace from chat suggestion")    

8. Now, let's introduce an error into the code to see how Copilot can fix it. Pick an instance of a variable name and change it to one that doesn't exist. For example, change an instance of "n" to "x". 

![introduce error](./images/cdd37b.png?raw=true "introduce error")   

9. Notice the light bulb icon that has popped up. Click on that, scroll to the bottom (if needed), and you'll have additional options to fix or explain with Copilot.

![Copilot options inline](./images/cdd165.png?raw=true "Copilot options inline")   

10. Go ahead and click on the "Fix using Copilot" option.

11. After a few moments, it should propose a fix that you can just accept (via the *Accept* button). You can also click on the *Show Changes* icon to see before/after for the proposed changes. (If it doesn't propose a fix in the dialog, you can skip to step 12 and use the /fix command in chat instead.)

![Fixing with Copilot](./images/cdd176.png?raw=true "Fixing with Copilot")       

12. (Optional) If you'd like, you can go back and make the error again, highlight the code, and then use the /fix command in the chat window to get the same results.

<p align="center">
**[END OF LAB]**
</p>
</br></br></br>

**Lab 3 - Using Copilot after the coding**

**Purpose: In this lab, we’ll see a few other ways to leverage Copilot after the initial coding is done**

1. Now that we have some code to work with, let's see what else Copilot can do for us. Let's have it explain the current code in our *prime.py* file.  Select the code. Then, use the **Cmd+I** keys to bring up the Copilot interactive chat dialog.

![Interactively telling Copilot to explain code](./images/cdd40b.png?raw=true "Interactively telling Copilot to explain code")


2. Tell Copilot to explain the code by typing the command below in the dialog. Hit Enter. Then, you should see the output in the dialog. Click on the *View in Chat* button to see the output in the separate chat window.

```
/explain
```

![Output of interactively telling Copilot to explain code in dialog](./images/cdd144.png?raw=true "Output of interactively telling Copilot to explain code in dialog")

![Output of interactively telling Copilot to explain code](./images/cdd177.png?raw=true "Output of interactively telling Copilot to explain code")

3. Now, let's do the same request but through a comment. In the *prime.py* file, below the code, on a new line, enter the following comment and hit Enter.
```
# explain the code above line-by-line
```
4. After this, Copilot should start showing the explanation in comments. Just hit tab to accept each line and then Enter to move to the next one until done. (Note that it might start repeating if you continue after it is done explaining the function the first time.)

![Output of telling Copilot to explain code via comment](./images/cdd42b.png?raw=true "Output of telling Copilot to explain code via comment")

5. We can also query Copilot inline via asking a question in a comment. Delete the commented explanation and try out the question below. To be clear you can prefix it with :q but that is not required with the chat feature installed.

```
# q: what does the function above do?
```

![Prompting for what code does with q:](./images/cdd43b.png?raw=true "Prompting for what code does with q:")

6. Finally, let's see how to use the doc feature to automatically document our code. Highlight the actual code.

7. Now, enter **Cmd+I** and enter the **/doc** command. After a few moments, Copilot should generate some documentation for the code. You can go ahead and *Accept* the changes.

![Generated doc for the code](./images/cdd44d.png?raw=true "Generated doc for the code")  

8. While this is useful documentation for the start of the function, we'd like to have more extensive comments in the function body. So,let's get Copilot's help with that. Bring up the chat dialog again with **Cmd+I** and enter the text "verbosely comment this code". After Copilot completes its suggestions, if you're happy with them, you can just click *Accept*. 

![Regenerating doc](./images/cdd110.png?raw=true "Regenerating doc")  

<p align="center">
**[END OF LAB]**
</p>
</br></br></br>

**Lab 4 - Using Copilot to generate tests**

**Purpose: In this lab, we'll see some examples of having Copilot generate tests**

1. Start out in the *prime.py* file we've been using. Position the cursor below the code.

2. Enter a comment to create unit tests
```
# create a function to do 5 unit tests of the code above
```

3. *If you don't get a suggestion*, enter code below to start nudging. Otherwise you can just accept the suggestion.

```
def test_is_prime():
```
![generating tests via comment](./images/cdd46a.png?raw=true "generating tests via comment") 

4. What if we didn't know how to test the code at all? Let's ask Copilot. Highlight the *is_prime()* function.

![selecting code](./images/cdd111.png?raw=true "selecting code") 

5. Now, switch to the chat interface and ask Copilot using the following prompt:

```
#selection How do I test this code?
```
![prompting on how to test](./images/cdd178.png?raw=true "prompting on how to test") 

(If you happen to encounter a dialog about confirming your testing environment, just hit *Accept* and run the query again.)

6. After entering this, you should see an explanation of how to test the code along with suggested testing code. If you expand the reference in the chat output, you can see that it used the selected lines.

![testing explanation](./images/cdd179.png?raw=true "testing explanation") 

7. Let's see what the shortcut command would do. In the main chat interface, enter "/tests" and then Enter. Copilot will want to add the *@workspace* agent onto the command. Just remove the *@workspace* from the beginning of the command. **Do not hit enter yet**.
```
/tests
```
8. Type a hash/sharp sign after /tests. At this point, Copilot should present a selection dialog. Choose #file from the menu using the keyboard arrow keys and Enter.
```
/tests #
```
   
![shortcut test command](./images/cdd140.png?raw=true "shortcut test command")

9. A dialog will pop up near the top of the codespace with a selection of files. Select the *prime.py* file to complete the command. 

![file choice dialog](./images/cdd141.png?raw=true "file choice dialog")

10. Once the command looks like */tests #file:prime.py*, go ahead and hit enter to see the suggested test results.

![Select to insert](./images/cdd167.png?raw=true "select to insert")

11. If you have a checkmark symbol in the chat output, select that. If you don't, hover over the code block, and in the popup menu, select the *...* entry and then the "Insert into New File" opton. 

![After insert](./images/cdd180.png?raw=true "after insert") 

12. After that, you'll have a new file in your editor with the code that you can save as needed (using the "3 bar" menu or the shortcut Ctrl/Cmd+S).

![Saving file](./images/cdd181.png?raw=true "saving file") 

13. We can also ask Copilot for other cases to test. Select the code in the testing file you just saved and, in the chat interface, prompt Copilot with

```
What other conditions should I test?
```

14. Copilot should respond with a list of other conditions to test and example code that you can add if you want.

![Additional conditions to test](./images/cdd186.png?raw=true "additional conditions to test") 

<p align="center">
**[END OF LAB]**
</p>
</br></br></br>

**Lab 5 - Using Copilot to help with SQL**

**Purpose: In this lab, we’ll see some examples of how to have Copilot help with writing SQL**

1. Create a new file named dev.sql. You can create it via entering the line below in the terminal.

```
code dev.sql
```
   
2. Afterwards this file should be open in a tab in the editor. Assume we want to work with a database or database definition that defines a dataset for students, staff, curriculums, courses, schools of study, locations, and registrations for a university system. Let's see what Copilot would generate for a query to get all students in a course - without any other context.

Enter the following comment below and press Tab to accept suggestions. Remember that you may have to hit Enter multiple times to get Copilot to prompt. Or if you don't get a suggestion or only get a comment, try "nudging" Copilot via typing "select". 

```
-- define a select statement to get all students enrolled in a course
```
3. Go ahead and save this file as part of the project.  You can do this from the "3-line" menu under File->Save, or just use the keyboard shortcut (Cmd + S | Ctrl + S)     

4. Let's see if we get any different results if we provide Copilot additional context. Open the file create-tables.sql in the editor from the GitHub repository. (You can either select and open it from the file list or use the command below from the terminal.) Scroll through it and take a quick look at the contents.

```
code create-tables.sql
```

5. Now with that file open, go back up to the top of the dev.sql file.  Highlight and delete the comment and resulting query from step 2.
  
6. Enter the same comment as before to request the query. (Basically, repeat step 2.) See what Copilot suggests this time. You can accept the suggestions or cycle through options. (If you first get a duplicate line as the query, just hit Enter and Copilot should start making more meaningful suggestions.)

```
-- define a select statement to get all students enrolled in a course
```

7. If all goes well, this second pass should generate a query with many more specific references to the names and identifiers used in *create-tables.sql*.  (If not, delete the result and try again.) Take a look at the query and then compare the names/identifiers used to the ones in the *create-tables.sql* file. This will show that Copilot picks up on context from other files available to it to make better suggestions.

![New query](./images/cdd97.png?raw=true "New query") 

   
8. In some cases, we might be able to use a separate index to speed up operations.  Let's ask Copilot to create a new index based on the last query. Add the following line after the current query in the file *dev.sql*.

```
-- write an index to improve the performance of the query
```
![index](./images/cdd98.png?raw=true "index") 

9. Let's suppose we also want to have a table to capture student attendance. We can ask Copilot to create the table definition for us.

```
-- define a table for student attendance to capture attendance by class
```

(Here again, if you don't get a meaningful response from Copilot, you may need to nudge it by typing *CREATE*.) In the definition Copilot provided, it may have added a comment for the status in the same format as the comment in the courses.registration table definition in the create-tables.sql file.

![status values](./images/cdd99.png?raw=true "status values") 

10. Copilot can also create stored procedures. Let's ask it to create a new stored procedure for getting a list of enrolled students at a particular location. Let's use the **CMD+I** shortcut. Go to the bottom of the *dev.sql* file, invoke Copilot Chat via the shortcut and then enter the line below in the dialog. You can also choose to change the model to Claude 3.5 Sonnet if you want. If you want to change the model, select it in the model drop-down, then you will probably need to select the *Enable* button and re-enter the prompt.  After the prompt is executed, you can choose to **Accept** or **Discard** the result.

```
define a stored procedure to get course enrollment by location
```
![prompt for stored procedure](./images/cdd182.png?raw=true "prompt for stored procedure") 
  
11. We can be more prescriptive with our stored procedure definition.  Let's add a more complex request. Go to the Chat interface and enter the prompt below.

```
define a stored procedure to get instructor details associated with a location
include instructor details, location details, and courses associated with the instructor
use instructor_id as the input parameter
```
![More extensive stored procedure definition](./images/cdd183.png?raw=true "More extensive stored procedure definition") 

12. Finally, let's see Copilot optimize a query for us. Suppose we want to get all the course registrations for September, 2023.  Enter the following query in the file.

```
select * from courses.registrations where year(registration_date) = 2023 and month(registration_date) = 9;
```

13. Ask Copilot to optimize the previous query. You can do this via highlighting the query (make sure to highlight the *entire* query), and in a chat interface enter "/optimize" in the dialog. You can Accept or Discard the suggested optimization after that.

```
/optimize
```
![Optimizing a query](./images/cdd184.png?raw=true "Optimizing a query") 

14. If you switched to the Claude 3.5 Sonnet model, you can switch back to the GPT 4o one if you want via the dropdown in the dialog.

![Switching models](./images/cdd185.png?raw=true "switching models") 
    
<p align="center">
**[END OF LAB]**
</p>
</br></br></br>

**Lab 6 - Teaching Copilot about updates**

**Purpose: In this lab, we’ll see an example of what to do when Copilot does not have the most up-to-date information**

1. Create a new file called *explore.go* via the same approach as you used to create other files.

2. This file should now be open in an editor tab. Let's say we want to seed a random number generator with Go. Let's ask Copilot to write a function to do that. Prompt it through the **CMD+I** interface using the statement below. Then you can accept the suggested code.

```
write a function to seed a random number generator
```
![Asking Copilot to write function to seed a random number generator](./images/cdd117.png?raw=true "Asking Copilot to write function to seed a random number generator") 

3. Copilot has probably generated code using the rand.Seed function. The challenge is that as of Go 1.20, the Seed function is deprecated.  Ref: https://cs.opensource.google/go/go/+/refs/tags/go1.21.0:src/math/rand/rand.go;l=394

4. Let's see if Copilot understands that this is deprecrated. We'll ask it via a query. Switch to the separate chat inferface and enter the query below.

```
Is the Seed function deprecated in Go?
```
![Is Seed function deprecated?](./images/cdd118.png?raw=true "Is Seed function deprecated?") 

5. Copilot probably responded with no and some info about the function. So one way we can help Copilot understand language updates is by providing the context in our file. So let's start again. Delete the current content in the explore.go file.

6. Now,let's provide Copilot some more direct context by copying in updated code examples. After deleting the code block from step 3, copy and paste in the following example of the replacement for the Seed deprecation into your explore.go file.  This is taken from pkg.go.dev/math/rand.

```
	// Create and seed the generator.
	// Typically a non-fixed seed should be used, such as time.Now().UnixNano().
	// Using a fixed seed will produce the same output on every run.
	// r := rand.New(rand.NewSource(99))
```

7. Now, let's try the creation of the function again. Underneath the comments and code you just pasted, invoke the dialog via **CMD+I** and enter the statement below again.
```
write a function to seed a random number generator
```

8. This time, the code should be using the same format and NewSource function as you put in the file in step 6. You can just Accept the change. (If you don't see a complete function, but just a single line, try changing the prompt to be "write a complete function to seed a random number generator".

![Updated random number gen code after including updated usage](./images/cdd119.png?raw=true "Updated random number gen code after including updated usage")

9. In preparation for the next lab, open a new chat by clicking on the "+" sign in the upper right part of the chat pane.

![New chat](./images/cdd187.png?raw=true "New chat") 

<p align="center">
**[END OF LAB]**
</p>
</br></br></br>

**Lab 7 - YAML generation, API use, translating code and the 2023 problem**

**Purpose: In this lab, we’ll learn about how to have Copilot help with YAML generation, API usage, translating code and explore the 2023 problem.**

1. Create a new file - **deployment.yaml**

```
code deployment.yaml
```

2. Bring up the Copilot Chat dialog via **CMD+I** and enter in the following request.

```
write spec for deployment in Kubernetes with 2 replicas and image from busybox
add command to run in containers: sleep 3600
add label app: myapp
add label type: front-end
```

3. After a few moments, you should see it respond with the code. You can just Accept this.
![Kubernetes manifest](./images/cdd120.png?raw=true "Kubernetes manifest")

4. Suppose we don't know how to execute this code. Let's ask Copilot. Highlight the generated YAML in the deployment.yaml file.  Then go to the larger Chat interface and ask it. Put the following in the Chat interface.

```
How do I execute this?
```

5. Copilot should respond with something like the following:

![How to execute deployment](./images/cdd188.png?raw=true "How to execute deployment")


6. While we're in the Chat interface, let's ask it for the latest K8s version. Put the following into the dialog. (If you get a *Request Failed* message, click on the *rerun without* link to *GitHub* above the error message.)

```
what is the latest Kubernetes version?
```

7. Notice that it identifies the latest version as as of October 2023. This highlights the out-of-date issue with the LLM.

![Answer to latest K8s version](./images/cdd189.png?raw=true "Answer to latest K8s version")


8. Let's have Copilot generate some code to work with Kubernetes through the API. In the chat interface, enter the following.

```
How do I call the K8s API for scaling a deployment to 5 replicas with Python?
```
9. The results may tell us that we first need to make sure something like PIP is installed. If so, we don't need to worry about this at the moment. Go to the actual generated code in the chat output. Click in that output area and paste the code into a new file via clicking on the "..." and then the *Insert into new file* menu option.

![Add code to new file](./images/cdd190.png?raw=true "Add code to new file")


10. Suppose we change our mind and want to convert this code to Go. Click in the new file, and highlight the new code. Then, in the Chat interface tell it to translate to Go. Then, look in the separate chat output and you should see the equivalent Go code available.

```
translate to Go 
```
![Go translation](./images/cdd125.png?raw=true "Go translation")

11. Optional - try changing the model in the chat interface to *Claude 3.5 Sonnet (Preview)* and ask the "latest version" question again with that model. (Don't forget to change it back if you want afterwards.)

```
what is the latest Kubernetes version?
```

<p align="center">
**[END OF LAB]**
</p>
</br></br></br>
    

**Lab 8 - Chat Participants**

**Purpose: In this lab, we'll see how to work with GitHub Copilot Chat Participants.**

1. Now let's see how Copilot can help with tasks using chat participants. First, we'll have Copilot help us commit a change.  Let's use the *explore.go* file we created in Lab 6. If you haven't already, make sure that file is saved.
   
2. Now, let's invoke the **@terminal** chat participant to ask a common question about how to stage your code changes. Go to the *chat* interface and enter the prompt below. Afterwards, the command to do the staging should show up in the chat output.

```
@terminal how do I stage explore.go?
```
![query output](./images/cdd134.png?raw=true "query output") 

3. Hover over the window with the commands in it, and then click on the icon that pops up for the terminal. Click on that to insert the command into the terminal. Then hit return.

![insert into terminal](./images/cdd171.png?raw=true "insert into terminal")


4. Now let's commit our change through the interface and have Copilot suggest a commit message for us. Click on the source control icon in the sidebar (#1 in the figure below). Your *explore.go* file should be selected. In the box titled "Message" above the *Commit bar*, click on the *sparkle icon* at the far right side (#2 in the figure below).

![insert into terminal](./images/cdd136.png?raw=true "insert into terminal")

5. After this, Copilot should (hopefully) generate an appropriate commit message in that box. Since we started the codespace via the button in the readme, you won't have direct commit access, so you can just proceed to the next step.

6. Now, let's switch gears and use the **@workspace** chat participant to help identify where we use certain things in our code. With the *explore.go* file still active in your editor, in the separate *chat* interface , enter the following prompt:

```
Which files are using SQL?
```

7. After executing this, you'll likely have some suggested information on how to search for files that use SQL in your project with search functionality for Visual Studio Code.
   
![initial query response](./images/cdd191.png?raw=true "initial query response")   

8. This is not the kind of answer we were looking for. Let's repeat the query with the *@workspace* chat participant.
```
@workspace Which files are using SQL?
```

9. After executing this, you should see Copilot assessing all of the files in the workspace and then returning a more specific and expected answer.
    
![more specific response](./images/cdd192.png?raw=true "more specific response")

<p align="center">
**[END OF LAB]**
</p>
</br></br></br>


**Lab 9 - Copilot in GitHub**

**Purpose: In this lab, we'll see how to use the integrated chat interface in GitHub.**

1. To give us a project to work with, we'll fork a repository from my GitHub area. Switch back to GitHub in the browser and go to https://github.com/skillrepos/sec-demo. 

2. Fork the skillsrepo/demo repository into your own GitHub space via the *Fork* button at the top right. Make sure to **uncheck** the *Copy the main branch only* box on the second screen.

![fork repo](./images/cdd172.png?raw=true "Fork repo")
![uncheck checkbox](./images/cdd147.png?raw=true "Uncheck checkbox")

3. After the fork is complete, in your fork, click on the *Chat with Copilot* button at the top right. The chat dialog will open up and then you will have a chat input box and some suggested questions. Click on the *Can you tell me about this repository?* question.  (If you don't see it, you can select one of the others or type in the question.) After this runs, you'll get some basic info about the repository.

 ![about the repo query](./images/cdd148.png?raw=true "About the repo query") 
 ![about the repo response](./images/cdd149.png?raw=true "About the repo response") 
 
4. Now, in the list of files in the repo, select the *main.go* file to open it up. In the chat dialog, start a new conversation by clicking on the "+" sign in the upper right of the dialog. This should switch the context to the file. Click on the *Summarize this file for me* question or type it into the input area. After this runs, you'll see a summarization of the file.

 ![about the file query](./images/cdd150.png?raw=true "About the file query") 
 ![about the file response](./images/cdd151.png?raw=true "About the file response") 
 
5. In this repo, we have a *dev* branch with some fixes for security vulnerabilities in the *main* branch. Let's create a pull request to merge the *dev* branch into the *main* branch. We could initiate the pull request manually, but since we have the Copilot Chat available, let's have it expedite the process by creating a simple link for us to use to start the pull request. In the Chat input area, tell Copilot to generate an appropriate URL via the prompt below and then submit it. After Copilot is done, you should see a link displayed.
```
Generate a url that I can use to create a pull request to merge the dev branch into the main branch
```

 ![generate pr link](./images/cdd152.png?raw=true "Generate pr link") 
 ![generated link](./images/cdd153.png?raw=true "Generated link") 
 
6. Click on the link in the chat dialog. This should open up a screen with a pull request initiated for merging the dev branch into the main branch. Close the Chat interface by clicking on the **X** symbol in the upper right corner of the dialog.

 ![collapse chat](./images/cdd193.png?raw=true "Collapse chat")  
  
7. In the pull request, update the title if you want. If you have one of the trial or paid plans, you can have Copilot automatically generate a description of our pull request. To do this, click on the *Copilot actions* button in the row under the *Add a description*. In the pop-up, select *Summary*. This will run for a few moments and then generate a draft summmary.

(Note: *If you are on the free (not trial) plan, you won't see the Copilot icon in the pull request area. If that's the case, you can just create the pull request, open up the "Files changed" tab, pick a change and go to step 10.*)

 ![generate summary](./images/cdd155.png?raw=true "Generate summary")  
 ![summary](./images/cdd156.png?raw=true "Summary")  
  
8. The summary will be in *markdown* format. You can click on the *Preview* button to see a readable presentation. When ready, click the *Create pull request* button to finish the creation.

 ![summary](./images/cdd157.png?raw=true "Summary") 

9. Notice that in the *Security Improvements* section, Copilot has generated links for each of the changes in the *models/models.go* file. Let's click on the 2nd link to look at those changes. (If you don't see the individual numbers, just click on the second list item.)

 ![looking at a change](./images/cdd158.png?raw=true "Looking at a change") 

10. This will open up the change comparison screen. Let's ask Copilot for some more information about the highlighted change. On the right of the screen will be a small, floating Copilot icon with a drop-down arrow. Click on that and select the *Explain* option. After this runs, you'll see an explanation of the highlighted section.

 ![request explanation](./images/cdd159.png?raw=true "Request explanation") 
 ![section explanation](./images/cdd160.png?raw=true "Section explanation")

11. Now, let's add a file to the context for the chat. Click on the *Ask Copilot* button at the top of the screen. In the *Select files to discuss* dialog, select *models/models.go*, check the box and then *Save* if the chat dialog is open or *Start Chat* if the dialog is not open. You'll then see the file attached as context in the Chat dialog.
    
![add file for context](./images/cdd161.png?raw=true "Add file for context")
![file added to context](./images/cdd162.png?raw=true "File added to context")

12. Finally, we'll prompt Copilot about why the changes need to be made. In the Chat input area, enter the prompt *Why do these changes need to be made?* It will use this file as context and respond accordingly. Notice in the screenshot below, the indicator for *1 reference - models.go*.
```
Why do these changes need to be made?
```
![answer with file as context](./images/cdd163.png?raw=true "Answer with file as context")

We're not going to go through and resolve the pull request, so you are done!

<p align="center">
**THANKS!**
</p>
</br></br></br>
 
# Appendix 1
## Alternate ways to "fork" repo if not allowed to use actual *Fork* button.

**Option 1 - Using Import**

1. Sign into GitHub if not already signed in.
   
2. Go to [**https://github.com/new/import**](https://github.com/new/import)
   
3. On that page, fill out the form as follows:
   
In "Your source repository details", in the "The URL for your source repository *" field, enter

```
https://github.com/skillrepos/sec-demo
```

Under "Your new repository details", make sure your userid shows up in the "Owner *" field and enter

```
sec-demo
```

in the "Repository name *" field.

The visibility field should be set to "Public".

![filling out form](./images/cdd195.png?raw=true "Filling out form")

4. If you haven't already, click on the green "Begin import" button.

5. After this, you should see the import processing... 

![import processing](./images/cdd196.png?raw=true "Import processing")

6. This will take several minutes to run. When done, you should see a "complete" message and your new
repo will be available. (There is a link in the complete message to click on to directly access it.)

![processing finished](./images/cdd197.png?raw=true "Processing finished")


**Option 2 - Using clone and push**

1. Sign into GitHub if not already signed in.

2. If you don't already have one, create a GitHub token or SSH key. If you are familiar with SSH keys, you can add your public key at
[**https://github.com/settings/keys**](https://github.com/settings/keys). Otherwise, you can just create a "classic" token by following the
instructions at [**https://docs.github.com/en/authentication/keeping-your-account-and-datasecure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic**](https://docs.github.com/en/authentication/keeping-your-account-and-datasecure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic). If you use a GitHub token, make sure to save a copy of it to use in the push step.

3. Clone down the [**skillrepos/greetings-ci**](https://github.com/skillrepos/greetings-ci) repository.

```
git clone https://github.com/skillrepos/greetings-ci (if using token)
```

or 

```
git clone git@github.com:skillrepos/greetings-ci (if using ssh)
```
4. Create a new repository in your GitHub space named *sec-demo*. Go to [**https://github.com/new**](https://github.com/new). Fill in
the "repo name" field with "sec-demo" and then click on the "Create repository" button.
   
![create new repo](./images/cdd198.png?raw=true "Create new repo")


5. On the page that comes up after that, select the appropriate protocol (https or ssh) and then follow
the instructions for "...or push an existing repository from the command line" to push your content
back to the GitHub repository. If you're using https you will be prompted for a password at push
time. Just paste in the classic token. (Note that for security reasons, you will not see the token
displayed.)

![push to repo](./images/cdd199.png?raw=true "Push to repo")
