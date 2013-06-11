*********
Git Intro
*********

.. s6:: styles

    h1: {fontSize:'150%', textAlign:'center', margin:'30% auto'}

Outline
=======
* How to start
  
  * install 
  * essential commands
  * tips
* concept of git
	
* what is github


How to start
============

win
	search git download
Mac
	brew install git
Ubuntu
	apt-get install git


All git commands	
================
how to know all command?

.. code-block:: bash

    git

Essential commands
==================

Commands you often use

.. code-block:: bash

    git clone
    git pull
    git push
    git add
    git checkout
    git status
    git log




Basic Tips
==========
type 

.. code-block:: bash

	git status

you will know what to do 


Concept of Git
==============

File Life Cycle
===============

.. image:: http://git-scm.com/figures/18333fig0201-tn.png
	:width: 90%
	:align: center

Init Repo
=========

You only do this at the first time

.. code-block:: bash

	mkdir sample
	cd sample
	git init .


Add Your Document
=================

Add Data

.. code-block:: bash

	echo '.' > sample.rst

See the status

.. code-block:: bash

    git status

Now What?
=========

Git Suggest you do git add

.. code-block:: bash

	# On branch master
	#
	# Initial commit
	#
	# Untracked files:
	#   (use "git add <file>..." to include in what will be committed)
	#
	#	sample.rst


I am good
=========

Do what git suggest

.. code-block:: bash

    git add sample.rst 

After enter stage area
======================


.. code-block:: bash

	# On branch master
	#
	# Initial commit
	#
	# Changes to be committed:
	#   (use "git rm --cached <file>..." to unstage)
	#
	#	new file:   sample.rst

Commit !
========

you need to write down some message

.. code-block:: bash

    git commit 

After Commit
============

check the status ..

.. code-block:: bash

    nothing to commit (working directory clean)

Edit Edit Edit
==============

Alter the content

.. code-block:: bash

    echo "secondtime" > sample.rst 

then ... what to do?

You have two choice
===================

Add or Discard

.. code-block:: bash

    git status  

"git add <file>...", to update what will be committed

"git checkout -- <file>...", to discard changes in working directory)



Git Basic Flow
==============
.. graphviz::
	
	digraph foo {
	  "git init"  -> "edit/git add";
	  "git clone" -> "edit/git add";
	  "edit/git add" -> "git commit";
	  "git commit" -> "edit/git add";
	  "git commit" -> "git push";
	}

GitHub
======

* Social Coding
* You Can Create Public Repo
* Clone Good Open Source Project
  
  * such as liang-in-django_ 
  
  .. _liang-in-django: https://github.com/TaipeiDjangoWorkShop/liang-in-django




Reference
=========

pro-git_ 

git-ready_ 

.. _git-ready: http://gitready.com/
.. _pro-git: http://git-scm.com/book









