Jenkins Job Creation: Implementing Version Control in Your CI/CD Pipeline

1.Creating the Jenkins Job

Opened Jenkins and clicked on “New Item”.
Created a Freestyle project and named it Newitem.
Under the Source Code Management section, selected Git.
Entered my GitHub repository URL: https://github.com/sneha-182003/Jenkins-task
Changed the branch specification from master to main, since my GitHub repo uses main as the default branch.

2. Adding Build Steps
   
In the Build section, I added a Windows batch command.
I used the following command to simulate a simple build: echo "Building the project..."
This command was added in the “Execute Windows batch command” section and used to verify that Jenkins executes the build step after cloning the repository.

3. Running the Build and Output
   
Clicked Build Now to trigger the build manually.
Viewed the logs under Console Output, which showed the following:

![image](https://github.com/user-attachments/assets/ba0ed371-4650-45b0-9d1b-8780f4490491)

This confirmed that Jenkins successfully:
Fetched the code from GitHub
Checked out the correct commit
Executed the batch command
Finished the build successfully

Challenges Faced and Solution

I initially got an error:
“Couldn't find any revision to build.”
This happened because Jenkins was looking for the master branch, which didn’t exist in my GitHub repo.
I resolved it by changing the branch specifier in Jenkins to main.

![image](https://github.com/user-attachments/assets/ed649bb6-f910-4701-a431-aa7f7917317e)

