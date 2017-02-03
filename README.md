# python-unittest-report-jenkins
This is the example of Python Unittest &amp; Coverage management with Jenkins Continuous Integration server.

<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/coverage-report.png"/>

# What to Use Jenkins for and When to Use It
Use Jenkins to automate your development workflow so you can focus on work that matters most. Jenkins is commonly used for:

- Building projects
- Running tests to detect bugs and other issues as soon as they are introduced
- Static code analysis
- Deployment
Execute repetitive tasks, save time, and optimize your development process with Jenkins.

# Manage python unittest with Jenkins in 9 Steps.

- you need to install jenkins and clone the repository. (install for ubuntu below)
```bash
wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
sudo service jenkins start
```
- open http://127.0.0.1:8080 and click Manage Jenkins
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/manage-plugin.png"/>
<br>
available tab - install cobertura plugin
- go back and click New Item (to follow the example of this repository, you can type "example")
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/newitem.png"/>
<br>
- give the permission to generate the report to the workspace for Jenkins and this repository
```bash
sudo chmod 777 /var/lib/jenkins/workspace/example
sudo chmod 777 ~/python-unittest-report-jenkins
```
- click example item - Configure.
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/homeexample.png"/>
<br>
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/examplestatus.png"/>
<br>
- edit shell and post build and save.
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/shell.png"/>
<br>
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/postbuild.png"/>
<br>
- click Build Now.
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/examplestatus.png"/>
<br>
- click the result(#1)
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/build.png"/>
<br>
- you can finally check the coverage report and unittest report.
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/coverage-report.png"/>
<br>
<br>
<img src="https://github.com/SkyHenryk/python-unittest-report-jenkins/blob/master/doc/pic/unittest-report.png"/>
<br>
