# exercicio01
b: 
    $git add arquivo.txt
    $ git status
        On branch main
        Your branch is up to date with 'origin/main'.      

        Changes to be committed:
          (use "git restore --staged <file>..." to unstage)
                new file:   arquivo.txt
c:
    $ git commit -m "git add example - arquivo.txt"
        [main 2df84ef] git add example - arquivo.txt
         Committer: JulioFigueredo-Impacta <julio.figueredo@aluno.faculdadeimpacta.com.br> 
        Your name and email address were configured automatically based    
        on your username and hostname. Please check that they are accurate.
        You can suppress this message by setting them explicitly:

            git config --global user.name "Your Name"
            git config --global user.email you@example.com

        After doing this, you may fix the identity used for this commit with:

           git commit --amend --reset-author

        1 file changed, 1 insertion(+)
        create mode 100644 arquivo.txt
e:
    $ git diff
        warning: in the working copy of 'arquivo.txt', LF will be replaced by CRLF the next time Git touches it
        diff --git a/arquivo.txt b/arquivo.txt
        index 8a0f05e..9e22bcb 100644
        --- a/arquivo.txt
        +++ b/arquivo.txt
        @@ -1 +1 @@
        -01
        +02
f:
    $ git add arquivo.txt
    $ git status
        On branch main
        Your branch is ahead of 'origin/main' by 1 commit.
          (use "git push" to publish your local commits)  

        Changes to be committed:
          (use "git restore --staged <file>..." to unstage)
                modified:   arquivo.txt
g:
    $ git diff
i:
    $ git diff
        warning: in the working copy of 'arquivo.txt', LF will be replaced by CRLF the next time Git touches it
        diff --git a/arquivo.txt b/arquivo.txt
        index 9e22bcb..75016ea 100644
        --- a/arquivo.txt
        +++ b/arquivo.txt
        @@ -1 +1 @@
        -02
        +03
j:
    $ git restore --staged arquivo.txt
    $ git diff
        warning: in the working copy of 'arquivo.txt', LF will be replaced by CRLF the next time Git touches it
        diff --git a/arquivo.txt b/arquivo.txt
        index 8a0f05e..75016ea 100644
        --- a/arquivo.txt
        +++ b/arquivo.txt
        @@ -1 +1 @@
        -01
        +03
k:
    $ git add arquivo.txt 
    $ git commit -m "echo arquivo.txt"
        [main f682269] echo arquivo.txt
         1 file changed, 1 insertion(+), 1 deletion(-)
    $ git log
        commit f68226965bd0353d12cb7c7ed21d239123e14a9b (HEAD -> main)
        Author: Julio Figueredo <julio.figueredo@aluno.faculdadeimpacta.com.br>
        Date:   Mon Aug 5 20:18:51 2024 -0300

            echo arquivo.txt

        commit d84c5abaa0ff9850399a2068b5ae2eba20d72b0b
        Author: Julio Figueredo <julio.figueredo@aluno.faculdadeimpacta.com.br>
        Date:   Mon Aug 5 20:11:58 2024 -0300

            git add example - arquivo.txt

        commit 0e4f293bf72932ed8cec78baf82c6b64278f877a (origin/main, origin/HEAD)
        Author: JulioFigueredo-Impacta <julio.figueredo@aluno.faculdadeimpacta.com.br>
        Date:   Mon Aug 5 20:03:30 2024 -0300

            Initial commit
m:
    $ git status
        On branch main
        Your branch is ahead of 'origin/main' by 2 commits.
          (use "git push" to publish your local commits)

        Untracked files:
          (use "git add <file>..." to include in what will be committed)
                .gitignore

        nothing added to commit but untracked files present (use "git add" to track)