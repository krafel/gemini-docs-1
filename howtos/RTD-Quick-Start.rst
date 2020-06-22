Quick Start Guide
=================

 **Convert docs to rst**

 1. ``pandoc --help`` Install pandoc if needed
 2. pdfs will have to be converted to docx using word
 2. ``pandoc -f docx -t rst filename.docx -o filename.rst`` typical pandoc usage
 3. ``pandoc -f docx -t rst filename.docx -o filename.rst --extract-media=./media`` convert doc with images
 4. or `write rst <https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_ 

  * Note: rst is indent aware like python 

 **Put docs in Gemini RTD Feasibility Git Repo**

 1. ``yum install git`` install git if needed
 2. ``git clone https://github.com/hstecher/gemini-rtd-feasibility.git`` clone the RTD study repo
 3. Copy rst files into the appropriate repo directory

  * ``pdfs/``
  * ``html/``
  * ``wiki/``
  * ``other/``

 4. ``git add <filename>`` add your new files to the repo
 5. ``vi pdfs/pdfs-index.rst`` edit the appropriate index.rst file to add your files to the end ::

   .. literalinclude:: ../pdfs/pdfs-index.rst 
      :language: rst
      :emphasize-lines: 8

 6. ``git commit filename.rst -m "comment"`` commit your changes
    ``git commit pdfs-index.rst -m "comment"``

 7. ``git push origin master`` push changest to github and trigger Read-The-Docs build

 8. After the ``git push`` Read-The-Docs will take a few minutes to upload your docs
 9. View updated `docs here <https://gemini-rtd-feasibility.readthedocs.io/en/latest/index.html>`_

  * The `github.com <https://www.github.com/hstecher/gemini-rtd-feasibility>`_ repo page will also have a link to the documents on Read-The-Docs

 **Additional Info**

 * `reStructuredText Primer <https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_

 * `TOC Tree usage <https://www.sphinx-doc.org/en/1.5/markup/toctree.html>`_ 
 
 * `Another rst guide <https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.htmltext#-formatting>`_ 


