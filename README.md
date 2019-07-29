# qthelplike-doxygen

Make Doxygen generated documentation readable in the Qt Help plugin.

**Note:** *In order to use this you need Doxygen already installed in your system.*

This is still a work in progress but at least the documentation should be readable in the Qt Creator help.



## How to

1. Create a `docs ` folder inside your project's folder (you should consider put this directory in the .gitignore file).

2. Copy the files `doxyfile.cfg` and `daaaxygenstyle.css` in that folder.

3. Change the following flags in order to document your own project (the paths are relative to the *doxyfile.cfg*:

   - `PROJECT_NAME`
   - `PROJECT_NUMBER`
   - `PROJECT_BRIEF`
   - `IMAGE_PATH` (PATH)
   - `HTML_EXTRA_FILES` (PATH)
   - `QHG_LOCATION` (PATH)
   - `INPUT` (PATH)
   - `QHP_NAMESPACE`

4. Run doxygen using the current configuration file as follows:

   ```
   doxygen doxyfile.cfg
   ```

5. The documentation should be generated in the `html` folder under the `docs` folder created before.

6. In order to associate the documentation in Qt Creator go to Preferences > Help, in Documentation click Add and select the file named `MyDoc.qch` under the `docs` folder.

   ![image](https://drive.google.com/uc?export=view&id=1SEUfKF0PJ2Xl4pNG29kWGMCpHlaMMnSH) 

7. Now you should be able to read the documentation of your project using the Qt Creator help.

