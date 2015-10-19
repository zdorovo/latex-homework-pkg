latex-homework-pkg
==================

A latex package for formatting statements of homework problems and subproblems

How to install this package
---------------------------

One way is to wave a copy of the .sty file in the same directory as the .tex files that use this package. Alternatively, you can save the .sty file to your texmf folder (see this tex.stackexchange post for details: http://tex.stackexchange.com/questions/1137/where-do-i-place-my-own-sty-files-to-make-them-available-to-all-my-tex-files)

To tell LaTeX you want to use this package, just write
\usepackage{homework}
in the preamble of your .tex file.

Syntax and output
-----------------

homework.sty keeps track of how many problems you've done. At the start of a new problem, write \prob[problem statement]. This will create a \subsection\* heading that reads "Problem (problem #)". The problem statement is written in italics below the \subsection\* heading. 

For subproblems, write \subp[(subproblem statement)]. This will create a vertical space and a new line (unless it's the first subproblem of a given problem---don't put stuff between the problem statement and the first subproblem). The next line will have a bold letter corresponding to the subproblem number (e.g. 'a' for the first subproblem) followed by the subproblem statement in italics and a new line. A horizontal space of 1ex is created after the bold letter, and a vertical space of 1ex is created between the subproblem statement and the text following it.

Bugs
----

You'll get a weird error if your problem statement has any sqauare brackets in it. To fix this, you should surround the problem statement with curly braces inside of the square brackets, i.e. \prob[{problem statement}]

To-do list
----------
Make subproblem numbers stick out into the left margin
Also, it would be better if problem number was optional. I should make a \prob\* command. Also, maybe the problem statement should be a required command---that would get rid of the square brackets issue. It's good practice to always write it, anyway. 
