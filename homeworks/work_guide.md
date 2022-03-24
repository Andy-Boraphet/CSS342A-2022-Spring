## Screen Recording

[Here](https://youtu.be/kpeFL7fLs-s) is a screen recording of the process described below for Mac OS.

## Checklist

[Here](https://github.com/a-teaching-goose/CSS342A-2022-Spring/blob/main/homeworks/submission_checklist.md) is a checklist for the process to be use during work. 

## Have a Github Account  

Create your own account at https://github.com/ if you don't have an account.

## Fork The Repo

- Fork (means "duplicate") the instructor repo https://github.com/a-teaching-goose/2022-342-sprint-1 to your own account.

- In the Action tab of the repo, click the green button to enable Action. If you missed this step, your PR won't run any test. You can still enable the Action any time later, and when you do, the PR test run can be triggered manually by close and reopen the PR.


## Open Repo in CLion

- Open your own repo in CLion using "Get From Version Control".

- Setup the configuration as shown here:

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/68986408/159604676-abaf5e56-6e5a-4c9f-afcd-a569ada22a82.png">

- Repeat after me: "Create a new branch called "work" (you can pick your own name here), and switch to this new branch (automatically in CLion)".
Read it out because this is a very popularly missed step, and the fix is not worth your time.

## Work On The Assignment Tasks

- Finish the homework in the "work" branch. Make commits and push frequently so your work is kept online safely. 

- The first time when you push online, CLion will ask you to log in with token or OATH. Token is the easiest way. [Here's an instruction](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/creating-a-personal-access-token). This will also be demo'd in lecture.

## Submission

- Once the homework is ready to for submission, head to your own repo on Github and create a pull request from your "work" branch towards ***your master branch***. 

  - Repeat after me: "DO NOT CREATE THE PULL REQUEST TOWARDS THE INSTRUCTOR'S REPO. TEST WILL FAIL IF YOU DO."

- Submit the url of your pull request in Canvas.

## After Due Date

- DO NOT make new code commits after submission deadline. If you do, your PR check will fail because one of the validation is about date violation. 

- Once grading is done, teacher will mark the PR as "approved" and grade will be published to Canvas.
