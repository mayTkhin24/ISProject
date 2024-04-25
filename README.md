**HOW TO ADD A NEW PROJECT OR A NEW FILTER**

_To add a new project or filter option to the Projects page of your website, you will need to update both the projects.json file and potentially the projects.html file, depending on whether you're adding a new filter category. Below is a step-by-step guide on how to perform each action.

**Adding a New Project**

_1. Update projects.json:_
Open projects.json in your preferred code editor.
Add a new object to the array with the following structure:

{
  "id": <next_sequential_id>,
  "partner": "<Partner_Name>",
  "year": "<Year_of_Project>",
  "course": ["<Course_Code>"],
  "representatives": ["<Representative_Name_1>", "<Representative_Name_2>"],
  "students": ["<Student_Name_1>", "<Student_Name_2>", "..."],
  "desc": "<Description_of_Project>",
  "logo": "<Path_to_Logo_Image>",
  "pdf": "<Path_to_Project_PDF>",
  "sdg": ["<sdg_1>", "<sdg_2>", "..."],
  "tech": ["<tech_1>", "<tech_2>", "..."]
}
* Replace placeholders with actual project details. Ensure image paths and PDF paths are correct and files are uploaded to the server.


_2. Commit and Push Changes:_
- Save your changes in projects.json.
- Use git add, git commit, and git push to push the changes to the GitHub repository.

**Adding a New Filter Option**

_1. Update projects.html:_
Locate the select element (<select>) for the filter category you want to add a new option to. For example, if adding a new Sustainable Development Goal (SDG) filter, locate the select element with id="sdg".
Add a new <option> element with the value set to the filter's identifier and the display text set to the filter name.

<option value="new_filter">New Filter Name</option>

_2. Update project-filter.js:_
If the filter is completely new (e.g., a new technology or SDG that was not previously listed), you will need to update the filtering logic in project-filter.js to account for the new filter. This may involve modifying the filteredProjects function to check for the new filter values.

_3. Test the Filters:_
Test the new filter on your local development environment to ensure it correctly filters the projects.

_4. Commit and Push Changes:_
Save your changes in projects.html and project-filter.js.
Use git add, git commit, and git push to push the changes to the GitHub repository.
After updating the repository, the live site should reflect these changes, provided the server is set up to automatically deploy or you have deployed the changes manually.

Notes:
Be careful with JSON syntax; ensure that commas, quotes, and brackets are correctly placed to avoid errors.
It's good practice to validate your JSON file after making changes to ensure there are no syntax errors.
Always back up your files before making significant changes.
For the new project details, ensure you have permissions to use any images or documents you are linking to.
