### Problem:
    jupyter nbconvert --to pdf my_notebook.ipynb

PDF conversion fails because of Latex error. But error is not shown...

### Solution
Inspiration: this gave me a lead that I should look for the log file and error output, but where though???    
https://stackoverflow.com/questions/62354358/failed-to-run-xelatex-notebook-tex-quiet-command-when-trying-to-download-ju

Look for this file.  
https://github.com/jupyter/nbconvert/blob/main/nbconvert/exporters/pdf.py

The problem lies in
      -quite

Removing it will give you the full error log output.

This should show the location of the nbconvert library:
        pip show nbconvert

Modify the file by removing the '-quite' element. You can then immediately run nbconvert.

Possible improvements:  
https://stackoverflow.com/questions/876239/how-to-redirect-and-append-both-standard-output-and-standard-error-to-a-file-wit  
https://stackoverflow.com/questions/29980798/where-does-pip-install-its-packages

Background:  
https://tex.stackexchange.com/questions/354518/what-does-the-emergency-stop-error-mean  
