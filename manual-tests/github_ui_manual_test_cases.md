#####Section: Sign Up and Login
---------------------------------
| Test Case ID | Description                    | Steps to Execute                                                                             | Expected Result                                       |
| ------------ | ------------------------------ | -------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| UI-001       | Login with valid credentials   | 1. Go to \[github.com/login]<br>2. Enter valid username and password<br>3. Click **Sign in** | User is logged in and redirected to the dashboard     |
| UI-002       | Login with invalid credentials | 1. Go to login page<br>2. Enter wrong password<br>3. Click **Sign in**                       | Error message shown: "Incorrect username or password" |
| UI-003       | Empty form submission          | 1. Click **Sign in** without entering anything                                               | Error messages shown below each field                 |
| UI-004       | Email field validation         | 1. Enter invalid email (e.g., `abc@com`) during sign-up                                      | Email validation error shown                          |

######Create New Repository
-----------------------------------------------
| Test Case ID | Description                        | Steps to Execute                                                                                     | Expected Result                                 |
| ------------ | ---------------------------------- | ---------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| UI-005       | Create public repo with valid name | 1. Login > Click **New Repo**<br>2. Enter valid repo name<br>3. Choose public<br>4. Click **Create** | Repo is created and redirected to the repo page |
| UI-006       | Invalid repo name                  | Enter repo name with special chars (like `#repo`)                                                    | Error: “Repository name is invalid”             |
| UI-007       | Duplicate repo name                | Try to create repo with existing name                                                                | Error: “Repository already exists”              |

--------------------------------------------
### Issue Tracking  
---------------------------
| Test Case ID | Description          | Steps to Execute                                                                                    | Expected Result                  |
| ------------ | -------------------- | --------------------------------------------------------------------------------------------------- | -------------------------------- |
| UI-008       | Create a new issue   | 1. Go to repository<br>2. Click **Issues** > **New Issue**<br>3. Enter title & description > Submit | Issue gets created and listed    |
| UI-009       | Add labels to issue  | 1. Open issue<br>2. Click **Labels**<br>3. Choose one or more labels                                | Labels are attached to the issue |
| UI-010       | Assign issue to user | 1. Open issue<br>2. Click **Assignees**<br>3. Select user                                           | Issue is assigned to that user   |
| UI-011       | Close an issue       | 1. Open issue<br>2. Click **Close issue**                                                           | Issue status changes to "Closed" |

--------------------------
#####Pull Request workflow
__________________________
| Test Case ID | Description           | Steps to Execute                                                                                                | Expected Result                        |
| ------------ | --------------------- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| UI-012       | Create a pull request | 1. Make changes in a new branch<br>2. Click **Pull Requests** > **New PR**<br>3. Choose base & compare branches | PR is created with proper diff preview |
| UI-013       | Review a pull request | 1. Open a PR<br>2. Click **Review changes** > Approve/Request changes                                           | Review comment is added                |
| UI-014       | Merge pull request    | 1. Open PR<br>2. Click **Merge**                                                                                | PR is merged and closed                |
| UI-015       | Check branch conflict | 1. Create PR with outdated base<br>2. Try to merge                                                              | GitHub shows a merge conflict error    |

### Repository Feature Navigation
| Test Case ID | Description                   | Steps to Execute                                                        | Expected Result                                         |
| ------------ | ----------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------- |
| UI-016       | Navigate to Code tab          | 1. Go to any repo<br>2. Click on **Code** tab                           | Repository code files are visible                       |
| UI-017       | Navigate to Issues tab        | 1. Go to any repo<br>2. Click on **Issues** tab                         | Issues list appears (if issues are enabled)             |
| UI-018       | Navigate to Pull Requests tab | 1. Go to any repo<br>2. Click on **Pull Requests** tab                  | List of PRs appears                                     |
| UI-019       | Navigate to Actions tab       | 1. Go to any repo<br>2. Click on **Actions** tab                        | GitHub Actions workflow (if any) is visible             |
| UI-020       | UI consistency across tabs    | 1. Navigate between **Code**, **Issues**, **PRs**, and **Actions**      | Header, sidebar, and footer layout should be consistent |
| UI-021       | Check loading time of tabs    | 1. Click each tab and measure load time                                 | Each tab loads within 2–3 seconds (ideally)             |
| UI-022       | Pagination in Issues tab      | 1. Go to Issues tab with more than 25 issues<br>2. Check bottom of list | Pagination buttons appear and function properly         |
