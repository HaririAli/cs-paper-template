# ResearchPaperTemplate

### A Latex template that minimises the repetitve work of styling and eleminate writing style-specific tex code.
###### The template supports IEEEtran and acmart styles only. However, I am planning to add support for more styles later.
---

To write a paper, you only need to your content in tex files under the *sections* directory.
It is recommended to write each section in separate tex file, but the template works pefectly fine if you write all content in one file.

Use the *variables.tex* file to define the title, abstract, keywords, document class (i.e. style), as well as the files in the *sections* directory that you would like them to be included.
Note that the files must be added in the same order you want them to appear.

Example of *variables.tex*:

    \def \varTitle{insert title here}
    \def \varAbstract{
	    insert abstract here
    }
    \def \varKeywords{
	    insert, comma-separated, keywords, here
    }
    \def \varDocClass{IEEEtran}
    \def \varKeyvals{conference}
    \def \varSections{introduction,section1,section2,conclusion}

Note that you only need to insert/modify the arguments of the above commands. Check *variables.tex*

In addition to the above, you need to define the authors in files specific to each style (e.g., *preamble/authorsIEEE.tex*).
This is the only place where you need to write style-specific tex code.
I need to find to way to allow author style to be configured dynamically such that users only define the authors and affiliations in the *variables.tex* file.
Feel free to contribute if you can help with this!

You can also use the *preamble/packages.tex* and *preamble/configUser.tex* to add packages and user-define preabmle code such as listings, filecontents, etc.

Finally, use *references.bib* for your bibliography.

---

Feel free to contribute by completing any of the **TODO** comments or by adding support for other styles.
