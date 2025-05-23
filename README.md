
<h1>File Integrity Monitor</h1>
This project outlines a demo of a File Integrity Monitor program using PowerShell ISE.<br />


<h2>How to:</h2>
Monitor File Integrity


<h2>Environments and Technologies Used</h2>

- PowerShell ISE

<h2>Operating Systems Used </h2>

- Windows 10

<h2>Stages</h2>

- Setup
- Baseline
- Monitoring
- Hash

<h2>Steps</h2>


<p>
<h2>Stage 1: Setup</h2>

Step 1: Temporarily allow script execution for the session.

![](media/ExecutionPolicy.png)

Step 2: Here is the Files folder we will be monitoring.

![](media/FilesFolder.png)

Step 3: Next, we run the custom script. (Found here: https://github.com/joshmadakor1/PowerShell-Integrity-FIM/blob/main/Fim.ps1)

![](media/RunScript.png)

</p>
<br />


<p>
<h2>Stage 2: Baseline</h2>

Step 4: Establish a new baseline on the files in the Files folder.

![](media/NewBaseline.png)

Step 5: Baseline file created. 

![](media/BaselineFile.png)

Step 6: File hashes of the four .txt files contained in the Files folder.

![](media/FileHash.png)

</p>
<br />


<p>
<h2>Stage 3: Monitoring</h2>

Step 7: Begin monitoring files using saved Baseline.

![](media/RerunProgram.png)

Step 8: After removing one of the files from the folder, we see that we get an alert that the file a.txt has been deleted.

![](media/FileDeleted.png)

Step 9: Then, I put the a.txt file back, but modified it by adding a new character, which the FIM detected and alerted us that the file had been changed.

![](media/FileChanged.png)

Step 10: I then added a new file called e.txt to the Files folder and received an alert that a new file had been created.

![](media/FileCreated.png)

</p>
<br />

<p>
<h2>Stage 4: Hash</h2>

Step 11: After returning the Files folder back to its original state, I output the SHA512 hash for the a.txt file.

![](media/aHash.png)

Step 12: By running the above command, I displayed the entire hash value.

![](media/Hashofa.png)

Step 13: Here we see the full hash of a.txt.

![](media/FullHash.png)

Step 14: Here I just added an additional a to the a.txt file.

![](media/Fourtha.png)

Step 15: And by running the same command as before, we can see that the file a.txt has a completely different hash since adding only 1 letter.

![](media/HashChange.png)

</p>
<br />
