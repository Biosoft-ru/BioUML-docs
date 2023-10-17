# BioUML-docs-ru
The BioUML platform documnetation in Russian

## For developer

1. Install Shinx.
<br/>```pip install sphinx```

2. Install recommonmark - it allows to use usual markdown for pages.
So it is not needed to convert already written pages.
<br/>```pip install recommonmark```

3. Install  Sphinx extension for rendering markdown tables.
<br/>```pip install sphinx_markdown_tables```

4. Install Read the Docs theme
<br/>```pip install sphinx-rtd-theme```

5. Install sphinx-intl
<br/>```pip install sphinx-intl```

6. ```make html``` - builds the project.
You can open in the browser generated html files fro 'target' directory.

7. When you pull you chages int github, the documentation on readthedocs will be automatically rebuilded due to hit webhook.

8. Open link
<br/>https://biouml.readthedocs.io
<br/>https://biouml.rtfd.io


#### Internationalization

1. Create pot files. They will be located in .\build\gettext directory.
<br/>```make gettext```

2. Create or update po files for English.
<br/>```sphinx-intl update -p build/gettext -l en```

3. Translate in Weblate

4. 

### References 

#### Sphinx
https://www.sphinx-doc.org/en/master/contents.html
<br/>https://www.sphinx-doc.org/en/master/usage/quickstart.html

#### RST
https://www.sphinx-doc.org/en/master/usage/restructuredtext/
<br/>https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html
<br/>https://runawayhorse001.github.io/SphinxGithub/rtxt.html

#### Kroki - to build different diagrams
https://kroki.io/
<br/>https://github.com/sphinx-contrib/kroki

#### Markdown 
http://recommonmark.readthedocs.org/
<br/>https://recommonmark.readthedocs.io/en/latest/auto_structify.html

https://github.com/ryanfox/sphinx-markdown-tables

#### Internationalization
https://www.sphinx-doc.org/en/master/usage/advanced/intl.html
<br/>https://docs.weblate.org/en/latest/devel/sphinx.html