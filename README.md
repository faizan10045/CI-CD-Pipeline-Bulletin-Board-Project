# Employee Bulletin Board Portal

Problem statement- Create a CICD pipeline for a Digital interactive Bulletin board application. 
Project is built using:-  
- HTML5 frontend, 
- Python/Flask as backend, 
- SQLAlchemy database, 
- CICD Pipleine having test stage (Lint test, PyTest), build stage (docker), deploy stage (Heroku), and final automated testing stage.

Pipeline Workflow
![image](https://user-images.githubusercontent.com/64662114/150958510-81b46b85-9d92-45a7-991b-8b421c907dab.png)

Demo:-
![CICD-project-recording](https://user-images.githubusercontent.com/64662114/150960128-fa31809c-f078-478b-b580-2bd8c2921272.gif)

STEPS:-
  1. Create empty project in GitLab then clone locally:- 
    "git clone https://gitlab.com/<repo-name>/<prj-name>.git"
  2. check ssh version using-   "ssh -V"
  in Finder- press Cmd+Shift+G. (Mac)	then serach “~.ssh/’	- to find ssh folder for already existing keys
  3. add the key in GitLab ssh section.
      "ssh -T git@gitlab.com"		- to verify if working properly
  4. create new branch- "git checkout -b back_end_models"
  5. Open VSCODE. Create a models folder and add model.py with SQLite code inside, then commit github as:-![image](https://user-images.githubusercontent.com/64662114/150961479-6afd6440-508c-4748-be1e-61e70fe5f13c.png)
  6. Then next git commit & push :-
 ![image](https://user-images.githubusercontent.com/64662114/150961595-2b9bfcb9-37c0-40a0-b3b0-2800fa43e98c.png)
  7. Next open gitlab. Create merge request to main. Approve & check changes in main
  8. Create templates, front-end, app-logic folder with codes and do:-
      "git add .", "git status", "git commit", "git push"
  9. Create .gitlab-ci.yml  file in VSCODE, add testing logic, then do above steps again and merge app-logic with main
    - "git checkout -b back_end_models"			->models folder
    - "git  checkout -b front_end_models"		->templates folder, req.txt, static folder
    - "git checkout -b app_logic"			->app.py, db creation
  10. type "python3" in terminal then type:- "from app import db", "db.create_all()", "exit()"
  11. "python3 app.py"			->to check app running on website
