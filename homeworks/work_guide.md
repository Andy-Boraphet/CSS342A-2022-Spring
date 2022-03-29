## Wow, So Many Steps!

It may seem tedious at the beginning, but after a few homeworks these will become muscle memories. This process is following a similar process how people work with real-life projects, so learning it will help you in a very long run.

You'll have at least 2 weeks to focus on getting comfortable with this. Take your time. Be patient.

## Screen Recording

[Here](https://youtu.be/kpeFL7fLs-s) is a screen recording of the process described below for Mac OS.

## Checklist

[Here](https://github.com/a-teaching-goose/CSS342A-2022-Spring/blob/main/homeworks/submission_checklist.md) is a checklist for the process to be use during work. 

## Have a Github Account  

Create your own account at https://github.com/ if you don't have an account.

## Softwares

Either MacOS or Windows, the following softwares need to be installed:

- CLion
- [Git](https://git-scm.com/downloads)
- Compilers
  - If you have **MacOS**: [XCode](https://developer.apple.com/xcode/)
  - else if **Windows**: [MingGW](https://www.mingw-w64.org/downloads/#mingw-builds) for compilers
  - else, talk to the instructor


## Fork The Repo

- Fork (means "duplicate") the instructor repo https://github.com/a-teaching-goose/2022-342-sprint-1 to your own account.

- In the Action tab of the repo, click the green button to enable Action. If you missed this step, your PR won't run any test. You can still enable the Action any time later, and when you do, the PR test run can be triggered manually by close and reopen the PR.


## Open Repo in CLion

- Open your own repo in CLion using "Get From Version Control".

- Setup the configuration:
 
For **Mac:** 

CMake:

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/68986408/159604676-abaf5e56-6e5a-4c9f-afcd-a569ada22a82.png">

Compilers:

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/252020/160519901-09f32f55-d8ad-4028-8482-3f24a3dd91ea.png">


For **Windows:**

CMake:

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/252020/160517403-60cd3213-be93-4c3d-aa76-0bc7bf16d9e3.png">

Compilers:

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/252020/160517570-4c2be64f-72eb-4c38-aee3-401ff257872b.png">


## Create a "work" branch

- Repeat after me: "Create a new branch called "work" (you can pick your own name here), and switch to this new branch (automatically in CLion)".
Read it out because this is a very popularly missed step, and the fix is not worth your time.

## Work On The Assignment Tasks

- Finish the homework in the "work" branch. Make commits and push frequently so your work is kept online safely. 

- The first time when you push online, CLion will ask you to log in with token or OATH. Token is the easiest way. [Here's an instruction](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/creating-a-personal-access-token). This will also be demo'd in lecture.

## Create a PR (Pull Request)

- Once the homework is ready to for submission, head to your own repo on Github and create a pull request from your "work" branch towards ***your master branch***. 

  - Repeat after me: "DO NOT CREATE THE PULL REQUEST TOWARDS THE INSTRUCTOR'S REPO. TEST WILL FAIL IF YOU DO."

## Submit the PR in Canvas

- Submit the url of your pull request in Canvas as homework

## After Due Date

- DO NOT make new code commits after submission deadline. If you do, your PR check will fail because one of the validation is about date violation. 

- Once grading is done, teacher will mark the PR as "approved" and grade will be published to Canvas.
