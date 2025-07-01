# IDE-rules
Rules files for agentic IDEs like Curor and Windsurf to get optimal performance out of your IDE assistant

## Step 1: Add rules and guidelines for humans in your projects README.md
- Housekeeping / best practices
- How to start the backend locally
- How to start the front end locally
- Instructions for local testing
- How to deploy the project
- How to view logs
- How to view Database Tables
- Differences per OS/environment

## Step 2: Copy the files from this repo to your project
- Copy the `global-rules.md` file to your IDE's global rules folder, or to the appropriate memories 
- Copy the `project-rules.md` file to your project's root folder, or to the appropriate memories location
- Ensure that the `project-rules.md` file is referenced in every prompt by turning this on in your IDE
- Copy the `project-structure.md` file to your project's root folder, or to the appropriate memories location
- Copy the `local_test` folder to your project's root folder
- **IMPORTANT:** gitignore the `local_test` folder in your project by adding `local_test` to your projects `.gitignore` file
- If relevant to your project, add API documentation links to the `api_docs` section of the `project-rules.md` file
- If relevant to your project, add example API curls to the `api_curls` folder
- If relevant to your project, add example API responses to the `api_responses` folder
- If relevant to your project, download .csv files for each database table that you will be working with and place them in the `database_tables` folder

## Step 3: Open your IDE chat and ask Gemini 2.5 Pro to update the files using the following prompt
```md
You are an expert Project architecture assistant.
Your job is to accurately describe a projects tech stack, structure, and intended functions.
You will take your time to reason in depth about the project and produce extremely accurate results.
You will need to:
- Review the tech stack of the project, and update the `project-structure.md` file
- Review the project structure, and update the `project-structure.md` file
- Accurately describe the Back end, the Front end, the Infrastructure, and any other components of the project
- Review the example api calls, responses, and database tables in the `local_test` folder
- Review the intended functions of the project, and update the relevant section of the `project-rules.md` file
- Accurately describe how each function is executed, and describe the relevant files and note their locations
```

## Step 4: Review and update the files manually
- AI will make mistakes and assumptions. A manual review is needed to ensure accuracy and will save a lot of time down the line.
- Update the tech stack of your project in the `project-structure.md` file
- Update your project structure in the `project-structure.md` file
- Update the Table names in the Database Scheme section of the `project-structure.md` file
- Update the project's intended functions in the `project_rules.md` file
- Update the rules in the `project_rules.md` file with anything specific to your project's needs


## Step 5: Use the prompts in the `local_test\prompts` folder for your development
- Always use a `checklist.md` file for each feature or change that will be implemented (Windsurf has this built in, so this is not required)
- Use the prompts in the `local_test\prompts` folder in the numbered order
- For every new feature or change, start with a `planning.md` prompt using the Gemini 2.5 Pro model
- Execute the `workflow.md` prompt using the Claude 4 model for rapid iterations, or Gemini 2.5 Pro for targeted changes
- Test using the `testing.md` prompts whenever a feature is completed
- Debug using the `debugging.md` prompts whenever an issue is encountered