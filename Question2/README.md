COMMAND 1:mkdir documents

OUTPUT:no output

EXPLANATION:This command creates a new directory named documents in the home directory.
It is used to organize project-related files in one place.
No output is shown because the directory was created successfully.




COMMAND 2:cd documents

OUTPUT:no output

EXPLANATION:This command changes the current working directory to documents.
It allows file operations to be performed inside this directory.
The absence of output indicates the directory change was successful.




COMMAND 3:touch plan.txt

OUTPUT:no output

EXPLANATION:This command creates an empty file named plan.txt.
It is used to store project-related notes or plans.
Since the file is created successfully, no output is displayed.




COMMAND 4:echo "This is my project plan file" > plan.txt

OUTPUT:no output

EXPLANATION:This command writes text into the plan.txt file using output redirection.
It overwrites the file content with the given project note.
The command produces no output because the text is written to the file.




COMMAND 5:ls -l plan.txt

OUTPUT:-rw-r--r-- 1 adhvaitha adhvaitha 29 plan.txt

EXPLANATION:This command displays file permissions, ownership, and size of plan.txt.
It confirms that the file belongs to the current user adhvaitha.
This verifies correct file creation and ownership.




COMMAND 6:cp plan.txt plan_copy.txt

OUTPUT:no output

EXPLANATION:This command creates a copy of plan.txt named plan_copy.txt.
It is useful for backup or version control purposes.
No output indicates the copy operation was successful.




COMMAND 7:cd ~

OUTPUT:no output

EXPLANATION:This command navigates back to the user’s home directory.
It prepares the environment for directory renaming.
The command executes silently when successful.




COMMAND 8:mv documents project_documents

OUTPUT:no output

EXPLANATION:This command renames the documents directory to project_documents.
It better reflects the directory’s purpose and project scope.
The rename is completed successfully without output.




COMMAND 9:mkdir project_documents/archive

OUTPUT:no output

EXPLANATION:This command creates a subdirectory named archive.
It is used to store backup or older versions of files.
The directory is created successfully without displaying output.




COMMAND 10:mv project_documents/plan_copy.txt project_documents/archive/

OUTPUT:no output

EXPLANATION:This command moves plan_copy.txt into the archive directory.
It helps in organizing files logically within the project.
No output means the file was moved successfully.




COMMAND 11:ls -R project_documents

OUTPUT:project_documents:
archive  plan.txt

project_documents/archive:
plan_copy.txt


EXPLANATION:This command lists all files and subdirectories recursively.
It shows the complete structure of project_documents.
This confirms proper file organization.




COMMAND 12:realpath project_documents/archive/plan_copy.txt

OUTPUT:/home/adhvaitha/project_documents/archive/plan_copy.txt

EXPLANATION:This command displays the absolute path of plan_copy.txt.
It confirms the file’s exact location in the filesystem.
This is useful for scripts and system-level operations.




