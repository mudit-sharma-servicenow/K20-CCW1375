# Work on ServiceNow application from within VS Code editor #
## Goal ##
If you want to do ServiceNow application development from comfort of your favorite editor, VS Code,
then this extension would enable you to do that.

## Application/Capabilities:
- App development from within VSCode

## Target Personas: ##
- Developer: Beginning ServiceNow Developer
- Developer: Experienced ServiceNow Developer
- Developer: Pro Developer New to ServiceNow

##Rest from below needs to be updated##

# About application #
We have two applications ## app1 ## and ## app2 ## created on the instance

# About VS Code extension #


## Pre-set up ##
1. Check for presence of node and it’s version
2. v 1.2.0 of extension has to be used for this lab.
3. VS Code version should be 1.44 or above.

##  Exercise 1 : Create project ##
1. Click on “Set up workspace” (ask to create a new folder) in the bottom toolbar
4. Create Project (users would enter credentials of assigned instance and import already created application)
5. Authentication type : Basic
6. Application type: Custom
7. Select *app1* from list of applications shown
8. Choose Script Include and Business rules as file types to import.
9. 
10. User are able the see downloaded files in explorer(must contain BR,SI,UI page. CS and ACL at least) <<img to be added>>
11. Study the options provided in the toolbar (talk about all of them) <<img to be added>> Sync changes (client to server)
12. User modifies logic in BR and syncs the project to instance
13. Verifies that change is reflected on the file in instance
14. executes the flow to verify that code changes are effective
15. User creates a new BR, BR1
16. Sync project and verify that the file is reflected on the instance    check the values in various fields in this BR.    talk about why we can’t capture multiple fields. Sync changes (server to client)
17. Make some changes in the BR on the instance (should not be a conflict scenario)
18. Go to extn and sync project
19. Changes made in file are reflected in the file on client. Conflict scenario
20. Make changes to BR1 on both client and server in same line to create a conflict
21. Sync project from extn to observe conflicts error thrown
22. Resolve conflict in each file on client side and sync again. 

## Exercise 2 : File Search ##
#Objective : Search for a file outside scope of current application and make modifications to it.#

1. Click on ‘File Search’ from toolbar
2. Choose the category to which the file belongs to ex: script include and business rule belong to server development
3. Select the file type
4. List of files of this type present on instance
5. Choose the files which you want to work on
6. Files are downloaded under Scratch folder in the project you are currently working in.
7. You can edit the file and sync it back to the instance using “Sync Current File” icon present at the top bar (next to file name)

## Exercise 3: Create multiple projects ##
#Objective : a) Demonstrate that user can create multiple projects in a single workspace.#
#            b) Demonstrate that different projects can use different authentication mechanisms while co-existing in same workspace.#

1. Get oAuth credentials : login to your instance and follow below steps 	  a) Navigate to System OAuth > Application Registry
		b) Create a new Application Registry.
		c) Under ‘What kind of OAuth application?’, choose ‘Create an OAuth API endpoint for external clients’
		d) Enter a name for the registry, Client Secret and hit save.
		e) The Client ID is an auto-populated field.

 Come back to VS Code window
1. Click on ‘Create project”
2. Enter  new URL, Select authentication type as oAuth, Enter username and password, Enter clientId and clientSecret (obtained in step above)
3. After authentication has succeeded chose app2 to import.

You now have 2 projects created in the workspace.

## Exercise 4: Chose update set for sync project ##
#Objective : Send your changes to desired update set#

1. Look at update set picker at the right hand corner of your toolbar at bottom it would show value as <<img to be added>>
2. Click on it and a pop-up would open up with open update sets in your current application.
3. Chose update set of your choice from the list.
4. Make some changes to a file and click “sync project”
5. Go to instance and verify that log for change is captured under your selected update set.

You can go to your other project, app1 and carry out similar exercise.
To switch to project app1, click on application picker at far right end of toolbar. It would show app2 as this is the current selected application.

## Exercise 5: Run background script  ##
#Objective : Demonstrate ability to run global and scope level background script#

<< Shasank please complete this >>


## Exercise 6: Compare a file to server ##
#Objective: Demonstrate ability to quickly show difference in state of a file on client from server #

1. Modify any file on your client (could be in either project).
2. Make some additional changes to the same by logging in to instance Noe you have some changes on client and some on server and both are unaware of each other.
3. Right click on the file name and select “Compare With Server”


##Exercise 7: Autocomplete##
#Objective: Demonstrate intellisense for JS and Jelly APIs.#
#			Demonstrate snippets (shortcuts)#
Advanced: Additional ServiceNow snippets from table ’Syntax Editor Macros’ are also supported.
Exercise: Add a new entry to Syntax Editor Macro Table and see if it reflects in extension snippets

##Exercise 8: Linting##
#Objective : Demonstrate that linting rules specified in platform are applied in extension.#

Make syntax errors and see they are highlighted accordingly

##Exercise 9 : Enable verbose logging from Settings page << Shasank please complete this >> ##
