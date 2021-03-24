# Automated-configuration-with-DSL-plugin
Task 1. Automated Deployments
Review
The stack of jobs will be created by automated way on public Jenkins http://ecsc00a017ac.epam.com/jenkins/ 
Task
1)	Install and configure DSL Plugin for the local Jenkins.
2)	Create jobs.groovy file (DSL script) for automated creation the following Jenkins jobs: 1 main and 4 child. 
3)	All scripts are stored in github repo https://github.com/Uladzimir-Kuchynski/d323dsl , Each student commits all step-by-step changes in own branch named {student}.

Where {student} is a first char from name + surname (all in lower case). Example: Aleksandr Mazurenko  = amazurenko

4)	Requirements for the jobs:
The main job :
This job is required to trigger the rest four from one place. It provides ability to choose jobs should be executed (by checkboxes) and predefine string parameter BRANCH_NAME which has two options: {student} (by default) and master. The main job should wait until all child jobs are executed and should be failing if even one of the triggered jobs is failed.
The child jobs:
a)	Each job has choice parameter BRANCH_NAME  with list of all branches available in repo https://github.com/Uladzimir-Kuchynski/d323dsl 
b)	The job should execute the cloned ‘script.sh’ from branch propagated by main job. Output should be saved to the file ‘output.txt’. The file should be attached to job.
c)	Templates cloned from appropriate branch should be archived to artefact ($BRANCH_NAME_dsl_script.tar.gz) and attached to each executed child job. 

Job name convention:
MNTLAB-{student}-main-build-job
MNTLAB-{student}-child1-build-job
MNTLAB-{student}-child2-build-job
MNTLAB-{student}-child3-build-job
MNTLAB-{student}-child4-build-job
Where {student} is a first char from name + surname (all in lower case). Example: Aleksandr Mazurenko  = amazurenko
