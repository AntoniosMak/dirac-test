Formative Assessment for the DiRAC Supercomputing Facility

Mike Jackson (Software Sustainability Institute, University of Edinburgh)
Greg Wilson (Software Carpentry)
James Hetherington (University College London)
Andrew Turner (University of Edinburgh)

= Introduction =

You have one hour to complete the following tasks.  

You may use the web, 'man' pages and any other resources you would
usually use when programming.  

If you are completing the assessment with colleagues, you are free
to discuss hints, tips and the usage of commands, but do not
share the answers to tasks.

If at any point you would like clarification, please do not hesitate
to ask.  

If at any point you are unable to complete a task, feel free to move
on to the next task.  The major tasks (shell, shell scripts,
testing, code review) are all independent.  You may ask for help
before moving on, but doing so will be considered equivalent to not
completing that task.

= Version Control =

You have just cloned a Git repository.  This serves as both a 
repository and your working copy.  You will do all of your work in 
this local repository, and use version control to commit your 
solutions as you go.

= Shell =

Use the cd command to go into the python/ directory.  Use a
single shell command to create a list of all files with names ending
in .dat in or below this directory in a file called 
all-dat-files.txt.

= Version Control =

Add all-dat-files.txt to the version control repository and commit
it.

Create a file, shell-command.txt, containing the command you ran
to get the list of files, add this to the version control repository
and commit it.

= Shell Scripts =

Write a shell script called do-many.sh that runs power2.py for many 
different numbers.  For example:

    ./do-many.sh 27 9 35

must produce:

    16
    8
    2
    1
    8
    1
    32
    2
    1

as its output.  You do not need to do error-checking on the
command-line parameters, i.e., you may assume that they are all
non-negative integers. 

= Version Control =

Add do-many.sh to the version control repository and commit it.

= Testing =

The analyze.py program contains a function called running_total, which
is supposed to calculate the total of each strictly increasing 
sequence of integers in a list:

    running_total([1, 2, 1, 8, 9, 2])       == [3, 18, 2]
    running_total([1, 3, 4, 2, 5, 4, 6, 9]) == [8, 7, 19]

In the file test_analyze.py, you will find a unit test implementing
the first example above. Write four (4) more unit tests that you think
are most important to run to test this function.  Do not test for
cases of invalid input (i.e., inputs that are strings, lists of lists,
or anything else that isn't a flat list of integers).

You can run your tests using the command:

    py.test test_analyze.py

= Version Control =

Add test_analyse.py to the version control repository.

= Code Review =

The program power2.py takes a single non-negative integer as a command
line argument and produces the powers of two that total to that
number.  For example:

    ./power2.py 27

produces:

    16
    8
    2
    1

Change this program in at least 3 ways to improve its readability,
understandability and modularity *without* changing its behavior. 

The file test_power2.py has tests for power2.py. You can check that
your changes have not changed power2.py's behaviour by running,

    py.test test_power2.py

= Version Control =

Commit your changes to power2.py to the version control repository.

= SSH keypairs =

Assume you have an account, username "me", on a remote host,
server.dirac.org. Password-based authentication to remote hosts are
vulnerable to brute-force attacks. SSH public key authentication
can provide you with additional security. 

Supposing you want to use a SSH public/private keypair, and
associated passphrase, to access the remote host, what commands would
you use to create your SSH keypair and to update the remote host with
your public key?

= Version Control =

Create a file, ssh-keypair.txt, with the commands you would use, and
add this to the version control repository.  

= Secure copy =

Assume that in your "me" account on server.dirac.org you have 100
files, detector001.dat, ..., detector099.dat, in a directory,
data. 

What commands would you use to securely copy the all the files from
server.dirac.org to your local account?

= Version Control =

Create a file, secure-copy.txt, with the commands you would use, and
add this to the version control repository. 

= Assesment Complete =

Please inform your examiner!
