# Test task #1
sudoku-master
to reproduce - you need

-git

-ant

-jenkins

install git

download https://github.com/VUMat/git-test1.git

copy dir to {JENKINS_HOME} (/var/lib/jenkins)

cd {dir git-test1-master}

create git repo inside and add our files:

git init

git add --all

git commit

install jenkins with plugins (Checkstyle Plug-in, Git plugin)

At jenkins create new project:

new item

\{name}\freestyle project

\Source Code Management - git

\file:///${JENKINS_HOME}/git-test1-master/.git

\Post-build Actions

\Add post-build action - Publish Checkstyle analysis results

\Checkstyle results - ' checkstyle_report.xml '

Build now

To show checkstyle report at dashboard:

Add new view

\add new column

\Number of Checkstyle warnings
