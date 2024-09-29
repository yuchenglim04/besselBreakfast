### Problem:
PDF conversion fails because of Latex error. But error is not shown...

### Solution
Look for this file.  
https://github.com/jupyter/nbconvert/blob/main/nbconvert/exporters/pdf.py

The problem lies in
  -quite

Removing it will give you the full error log output.

This should show the location of the nbconvert library:
  pip show nbconvert

Modify the file by removing the '-quite' element. You can then immediately run nbconvert.
