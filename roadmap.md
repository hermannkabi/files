# Roadmap for the Files project

## What is the Files project?
Simply put, the Files web app will be loacted in [hermannkabi.com/files](hermannkabi.com/files). It will be an easy way to read files and folders put in the [scripts](https://github.com/hermannkabi/files/tree/main/scripts) folder of the [files](https://github.com/hermannkabi/files) repo, and also for accessing all my repos.

## Roadmap

1. The basic logic:
    1) GET the Github API for the path /users/hermannkabi/repos to get all of the repos.
    2) For each repo, make a card and add it to the list to show.
    3) Now, GET the Github API for the path /repos/hermannkabi/files/contents/scripts/ to get all the files from the [scripts](https://github.com/hermannkabi/files/tree/main/scripts) folder of the [files](https://github.com/hermannkabi/files) repo.
    4) If a file has type="dir", then that will be a folder.
    5) Add all of the files (type="file") to the list to show (add a subtitle of path)
    6) Add all of the folders (type="dir") to the list to show (add a subtitle of path). When clicking on the folder, GET /repos/hermannkabi/files/contents/scripts/PROJECT_NAME and clear the list to show
    7) Because the format is same, you just need to call the method with the parameter of /repos/hermannkabi/files/contents/scripts/PROJECT_NAME and it will do the rest
    8) Going back is exactly the same, if the url doesn't end with scritps, just split the path at the last /
    
