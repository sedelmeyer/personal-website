sedelmeyer.net
==============

**This is me on the internet!**

Summary
-------

This repository contains the source code and raw reStructuredText_ content used to generate my personal website. This website is located at: http://www.sedelmeyer.net/

This site is implemented using Sphinx_ as a static site generator. To view the resulting Sphinx-generated html content, please see the ``gh-pages`` git branch for this project: https://github.com/sedelmeyer/website/tree/gh-pages

Workflows and requirements
--------------------------

Documented below, so I do not forget them, are workflow and requirements related to my management of this site.

.. contents:: Sections
    :local:
    :depth: 2
    :backlinks: top 

Publishing to ``gh-pages``
^^^^^^^^^^^^^^^^^^^^^^^^^^

The basic steps for publishing Sphinx-generated site content to GitHub pages content are as follows:

* After running ``make html`` to generate site content, first create an orphaned ``gh-pages`` branch. Note that this only needs to be done once to create the branch::

    git checkout --orphaned gh-pages

* By default, all existing files not excluded by ``.gitignore`` will be staged in the new branch. Remove them all from staging with this command::

    git rm --cached -r .

* Once they're removed from staging and no longer tracked by Git, delete them from the gh-pages branch all together. (they will still exist on the ``master`` branch.)::

    git clean -id

* A prompt will appear. The command to specify is ``c`` (clean). By cleaning the repo, the ``gh-pages`` branch will be left containing only the ``.git/`` directory, as well as any other files previously ignored by Git as specified by the ``.gitignore`` file (including the ``docs/_build/html/`` site content).

* Now, to be certain not to delete or commit any of the other files previously ignored by Git on the ``master`` branch (because these will vanish from the ``master`` branch too if accidentally deleted), checkout the master version of ``.gitignore``::

    git checkout master -- .gitignore

* Running ``git status`` shows that this command has placed the master .gitignore in the ``gh-pages`` staging area, and that Git has gone back to ignoring the other files as they were on the ``master`` branch. Commit it as such::

    git commit -m "git: add .gitignore from master"

* Now to place all of Sphinx-generated site content into the ``gh-pages`` base directory for rendering by GitHub Pages::

    cp -r docs/_build/html/* .

* Next, add a blank ``.nojekyll`` file to the directory to tell GitHub that this is not a Jekyll-generated site::

    touch .nojekyll

* Check ``git status`` to see that the site content is now visible to git because it has been taken out of the previously ignored ``docs/_build/`` directory.

* Add the site content files to Git staging and commit them::

    git add -A
    git commit -m "docs: add <current release version> site content"

* Then, push the changes to GitHub::

    git push origin gh-pages

* Once committed and pushed, return to any of the other branches to continue work on the website::

    git checkout master

* Next site content needs to be updated on ``gh-pages``, checkout the ``gh-pages`` branch and follow the above outlined process again starting with the step of copying over the latest .gitignore in case any edits were made to it on ``master``::

    git checkout gh-pages
    git checkout master -- .gitignore
    ...

Resizing images using ImageMagik
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Images for this site can be batch resized to a suitable size for web publishing using the command line application ImageMagik_. A simple workflow for accomplishing this is outlined below. Please note that thus far, this command has only been tested using ImageMagik version 6.9.7-4:

1. Save all full-resolution image files to a local directory.
2. Use ImageMagik's ``mogrify`` to batch resize all images in that "input" directory to a different "output" directory::

    mogrify -path OUTPUT_DIR -filter Triangle -define filter:support=2 \
    -thumbnail 700x700 -unsharp 0.25x0.25+8+0.065 -dither None \
    -posterize 136 -quality 82 -define jpeg:fancy-upsampling=off \
    -define png:compression-filter=5 -define png:compression-level=9 \
    -define png:compression-strategy=1 -define png:exclude-chunk=all \
    -interlace none -colorspace sRGB -strip INPUT_DIR/*.EXT

3. The resulting output directory can be saved to the ``./docs/_static/img/`` directory for publishing on this site.

Special thanks to `Dave Newton <https://github.com/nwtn>`_, for publishing this well-tested ``mogrify`` ImageMagik command waaaay back in 2015 in `his excellent smashingmagazine.com article <https://www.smashingmagazine.com/2015/06/efficient-image-resizing-with-imagemagick/>`_! 


.. _Sphinx: https://www.sphinx-doc.org/en/master/index.html
.. _reStructuredText: https://docutils.sourceforge.io/rst.html
.. _ImageMagik: https://imagemagick.org/index.php