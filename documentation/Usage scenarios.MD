## Prerequisites 

- Launch Pharo Image

- Open Hyalinos

![My Image](https://github.com/hyalinos/icpc/blob/main/sreenshots/open.png)

The following menu will open

![My Image](https://github.com/hyalinos/icpc/blob/main/sreenshots/menu.png)

# 1. Run inference on a package

- Choose 'Run Inference' from the menu

![My Image](https://github.com/hyalinos/icpc/blob/main/sreenshots/inference_menu.png)

- In the 'Scope and configuration menu' add some packages to the right column, choose 1 or several inference tools and merging strategy. Below there is an example of a configuration.

![My Image](https://github.com/hyalinos/icpc/blob/main/sreenshots/inference_configuration.png)

- Press run

When inference will be complete (might take some time depending on the amount and matter of packages under analysis), 'Browse results' window with inference results.

![My Image](https://github.com/hyalinos/icpc/blob/main/sreenshots/inference_results.png)

2. Subscribe all new repositories to trigger the inference when they are commited

- Open Hyalinos
- Click on Subscribe repositories
- Check 'Subscribe all future repositories'
- Save
- Open Iceberg repositories manager (Sources -> Git repositories browser)
- Click 'Add'
- Choose 'Clone remote repository'
- Enter repository address: https://github.com/hyalinos/test-project.git and click on 'Ok'
- Choose 'test-project' in the list of loaded repositories and double click on it.
- Right-click on the package 'HyTestPackage' -> Load.
- Double-click on 'HyTestPackage'. System Browser will open where you can change the code.
- Click on 'HyTestClass' and then on 'hello' method.
- Change the string ^ 'hello there' of the method.
- Double-click -> Accept to save changes
- Go back to the list of Iceberg repositories, double-click on 'test-project'.
- Click on 'Commit' button -> Commit
- When commiting process is finished, inference will start automatically. It will not display the results but they can be found in the 'Browse Results' table of Hyalinos tool






