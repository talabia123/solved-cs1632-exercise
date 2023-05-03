Download Link: https://assignmentchef.com/product/solved-cs1632-exercise
<br>
The purpose of this exercise is to assess your Java programming skills cominginto this class. Please submit by Wednesday 11:59 PM so that I may give youfeedback before the add/drop deadline. I may recommend that some of you dropthe course if your programming skills are not up to par. Submission of thisexercise will take the place of attendance today. The actual score will onlybe used to measure your pre-existing skills and will not count towards thefinal grade.

Another purpose of this exercise is to familiarize you with the workflow forthis course. We are going to use GitHub for collaboration and source codeversioning, and also for submitting to GradeScope. Once your code is submittedto GradeSCope, the autograder will automatically test your code and assign ascore depending upon the pass/fail of each test case. The autograder will alsogive you valuable feedback on the deductions you got so that you can fix yourmistakes and resubmit to get a higher score. There is no limit to the numberof submissions.

Please follow the below instructions.

## Install JDK 8

The official Java version for this class is Java 8 (1.8.0.231). Please install the Java package for your OS at:

https://drive.google.com/drive/folders/1E76H7y2nMsrdiBwJi0nwlzczAgTKKhv7

After installation, make sure you have the correct Java and Javac versions by doing “java-version” and “javac -version”. You should get something like the following:

“`$ java -versionjava version “1.8.0_231”Java(TM) SE Runtime Environment (build 1.8.0_231-b11)Java HotSpot(TM) 64-Bit Server VM (build 25.231-b11, mixed mode)“`

Alternatively, you can use these versions of OpenJDK 8 that have been verified to work with our tool chain:* https://chocolatey.org/packages/openjdk8* https://chocolatey.org/packages/zulu8

After installing, they should show their respective versions on “java -version”. For example, for zulu8:“`$ java -versionopenjdk version “1.8.0_265”OpenJDK Runtime Environment (Zulu 8.48.0.53-CA-win64) (build 1.8.0_265-b11)OpenJDK 64-Bit Server VM (Zulu 8.48.0.53-CA-win64) (build 25.265-b11, mixed mode)“`

If you don’t see the correct version (either for JDK 8, OpenJDK 8, or Zulu 8), please follow the below instructions toset up the Path OS environment variable.

### Setting up JDK 8 for Windows

1. Search “environment” in the Windows 10 search box.2. Open “Edit the system environment variables” control panel.3. Click on the “Environment Variables” box.4. Search the “Path” environment variable in user variables and system variables.5. Add the bin directory of the Java installation, probably “C:Program FilesJavajdk1.8.0_231bin” to the top of the “Path”6. For good measure, you may want to remove other Java installations from the “Path”7. After this, try doing “java -version” again and it should have changed.

If you use [Chocolatey](https://chocolatey.org/) as your package manager, and you opted to install OpenJDK 8, you will have to replace the above Java bin path with the path where Chocolatey installs the package.

### Setting up JDK 8 for MacOS

1. Open ~/.bash_profile with your favorite editor (if you don’t have one, just do “pico ~/.bash_profile”)2. Add the following 2 lines at the bottomexport PATH=/Library/Java/JavaVirtualMachines/jdk1.8.0_231.jdk/Contents/Home/bin:$PATHexport JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_231.jdk/Contents/Home/3. Save the file and exit from the terminal4. Relaunch the terminal and try doing “which java”. It should say /Library/Java/JavaVirtualMachines/jdk1.8.0_231.jdk/Contents/Home/bin/java.5. Now you are good to go! Otherwise, try doing “echo $PATH” and see if your path is not updated properly, or if there is some other Java installation before you.

Alternatively, you can use [jEnv](https://www.jenv.be/) that allows you to switch Java versions easily on a Mac. You will also need [Mac brew](https://brew.sh/) if you don’t already have it. These are just one liners to install so it should be pretty painless.

It’s a brew installation so it should be pretty painless.

## Create GitHub Repository

For every source code submission in this class, you are asked to create a newGitHub repository. If you don’t already have a GitHub account, please createone.

1. If you are new to git source versioning or GitHub, I recommend that youstart by using the Desktop GUI version. You can download it from:

https://desktop.github.com/

2. Once you’ve installed GitHub Desktop, let’s first clone the course repository to your computer:

https://help.github.com/en/desktop/contributing-to-projects/cloning-a-repository-from-github-to-github-desktop

You will need to go to the root of the course repository to get the clone link:

https://github.com/wonsunahn/CS1632_Fall2020

This way, you will have always have up=to-date course materials on yourcomputer. Whenever there are updates to the course materials, the “Pull”request button will be activated for the repository on GitHub Desktop. Clickingthat button will bring your local folder in sync with the updated materials.

3. Next, create a new repository just for this exercise:

https://help.github.com/en/desktop/getting-started-with-github-desktop/creating-your-first-repository-using-github-desktop

You can name it whatever you want (but preferably something easy to remember, right?).

Once you’ve created the repository, copy over the contents of just the exercisefolder in the course repository to the new repository folder. Once you’vecopied over the files, you need to “Commit” and “Push” the files to uploadthose files to GitHub. If you are successful, you should be able to see yournew repository with the new files at github.com.

4. Whenever you make improvements to your source code, frequently “Commit” and“Push” those changes to GitHub so that your new changes are versioned.

## Compilation

Go to the new repository folder you created for this exercise and make sure that the Java file compiles:

“`$ mkdir bin$ javac -d bin src/*.java

“`

You should see no errors at this point

## Running

Try running the compiled class file:

“`$ java -cp bin SortedCollectionUsage: java SortedCollection [num1] [num2] [num3] …“`

The SortedCollection main method just prints usage information when nocommandline arguments are passed. With commandline arguments, it should printout the commandline arguments in sorted order, from smallest to largest:

“`$ java -cp bin SortedCollection 3 2 1sorted: 1 2 3“`

But at the current state, SortedCollection is incomplete and prints out:

“`$ java -cp bin SortedCollection 3 2 1sorted: 0 0 0“`

Your job is to complete SortedCollection so that it works properly.

## Completing SortedCollection.java

The places in source code where you are asked to insert or modify code aremarked by // TODO comments. Feel free to use any data structure from java.utilor one of your own. It doesn’t matter how you implement it as long as it worksas specified. Pay attention to the Javadoc comments on top of each method.

## Submission

You will do GitHub submission to GradeScope.

1. By now you should have created a new github repository just for thisexercise. Make sure you keep the repository *PRIVATE* so that nobody elsecan access your repository. Once you are done modifying code, don’t forget tocommit and push your changes to the github repository.

2. When you are done, submit your github repository to GradeScope at the “JavaAssessment Exercise” link. Once you submit, GradeScope will run theautograder to grade you and give feedback. If you get deductions, fix yourcode based on the feedback and resubmit. Repeat until you don’t getdeductions.

Please submit by Wednesday (5/13) 11:59 PM to count towards attendance.

IMPORTANT: Please keep the github private! This applies to all future submissions.

## GradeScope Feedback

GradeScope feedback is your friend. Submit as many times as you want to getfrequent feedback. There are 10 tests for this exercise and if there is anerror, the error message will tell you what was expected what was observed.When the compared value is a string, brackets ([, ]) are used to annotateexactly which part of the two strings differed.

The tests were done using an automated testing infrastructure called JUnit thatallows you to rigorously test software. You will eventually learn to use thistool too as part of this course!

## Resources

* JDK 8 installation packages:https://drive.google.com/drive/folders/1E76H7y2nMsrdiBwJi0nwlzczAgTKKhv7

* Java 8 API reference manual:https://docs.oracle.com/javase/8/docs/api/overview-summary.html