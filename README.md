andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1$ mkdir A
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1$ cd A
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ git init
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ echo '' > fileA.txt
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ echo '' > fileB.txt
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ git add .
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ git commit 
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ git checkout -b branch1
Switched to a new branch 'branch1'
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ git clone . ../B
Cloning into '../B'...
done.
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ git checkout master 
M	fileA.txt
M	fileB.txt
Switched to branch 'master'
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/A$ cd ../B
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/B$ git checkout branch1 
Already on 'branch1'
Your branch is up-to-date with 'origin/branch1'.
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/B$ echo '' > fileC.txt
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/B$ git add .
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/lab1/B$ git commit 
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/B$ git push origin branch1 
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 262 bytes | 0 bytes/s, done.
Total 2 (delta 1), reused 0 (delta 0)
To /home/andrew/Desktop/hh/git/.
   b406a14..4c4e480  branch1 -> branch1
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/B$ cd ../A
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/A$ git checkout branch1 
D	3
D	lab1/commands.txt
Switched to branch 'branch1'
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/A$ echo 'line1' > fileC.txt
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/A$ git add .
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/A$ git commit
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/B$ echo 'line1' > fileC.txt
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/B$ git add .
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/B$ git commit
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/B$ git fetch
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/B$ git merge origin/branch1 
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/B$ git remote remove origin
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/B$ cd ../A
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/A$ git remote add origin ../B
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/A$ git fetch
remote: Counting objects: 2, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 1), reused 0 (delta 0)
Unpacking objects: 100% (2/2), done.
From ../B
 * [new branch]      branch1    -> origin/branch1
 * [new branch]      master     -> origin/master
andrew@HP-ENVY-m6-Notebook-PC:~/Desktop/hh/git/A$ git merge origin/branch1 
Updating 3e7c1fd..122e598
Fast-forward
