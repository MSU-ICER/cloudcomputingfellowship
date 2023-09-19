## Website for the MSU Computing CloudFellowship

Website: https://msu-icer.github.io/cloudcomputingfellowship/

This is the source code for the building the website and materials for the 2023-2024 MSU Cloud Computing Fellowship, used by the fellowship organizers.   Students do not need to use this source code, simply visit the site above.  

See the home page of the site for information about the Cloud Computing Fellowship, or contact https://icer.msu.edu
 

### Building

The site was build with the amazing python package "MkDocs" and Markdown: [mkdocs.org](https://www.mkdocs.org).  The theme is the also amazing https://github.com/squidfunk/mkdocs-material

Mkdocs has a 'gh-deploy' command that uses the "gh pages branch" method (rather than the new github workflows method).   Hence this github project uses a branch for github pages

Procedures to collaborate: 

1. fork the github repository from into your own space
2. clone the forked repository

`git clone git@github.com:<youruserid>/cloudcomputingfellowship.git`

3. Install requirements

```
cd cloudcomputingfellowship
# optionally but recommended: create a python environment
# this example uses virtualenv , but you could use conda, etc
virtualenv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

4. viewing the site. 

```
mkdocs serve
```

Will open a server on on your computer to preview the site. See https://www.mkdocs.org/getting-started/  

If you just want to build you can use  `mkdocs build`  in either case, the site will be rendered into a folder `site`  This folder is not included in the github repository, only `\docs`  (see the `.gitignore ` file). 

If there are warnings or issues with the render, they will be shown in the terminal but the site will still render unless there is a catastrophic error. 

All of the site content is in the `/docs` folder and can be edited while serving and should update. 


### Current Collaborating Process

1. create a github issue for a problems, improvements or new content in the parent repository (in the MSU-ICER domain). 
2. in your clone of the repository, create an issue branch, starting with the number of the issue.  
3. when commiting, reference the issue in teh commit message, e.g. "fixes #2"
4. when the issue is addressed in the branch, create a pull request (PR)
5. someone else should review the changes if available merge the PR t into the main repository main branch
6. once merged into the main repository, deploy from there to gh pages
7. sync your fork using github
8. pull the main branch to your laptop

---

Licensed as Creative Commons Attribution-NonCommercial 4.0 International License

![Creative Commons License](https://i.creativecommons.org/l/by-nc/4.0/88x31.png)

http://creativecommons.org/licenses/by-nc/4.0/
