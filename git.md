# GIT MAGIC
*** by Pierre-Louis Palant ***
* Collected from various sources *
---

## Untrack newly .gitignore'd files
 - Commit everything, especially new .gitignore
 - remove everything:
    - ```git rm -r --cached .```
        - *translation: recursive (-r) removal (rm) of all files (.) from the index only (--cached)*
 - Re add everything again (this will apply .gitignore)
    - ```git add .```
  - Commit your changes:
    - ```git commit -m "Applied new .gitignore"```
  - Done!

