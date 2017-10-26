# bestpracticesR

## Best practices for reproducible coding in R

![humor](http://imgs.xkcd.com/comics/code_quality.png)

## Setting up your folder structure
* one folder per project = one contained unit
  * definition of “contained unit” depends on your project, style, requirements
* make sure that this is your working directory in R/R Studio
* Examples of folder structures to use [http://nicercode.github.io/blog/2013-04-05-projects]
### R/
* contains analysis script
 * often used functions (potentially in different function script file)
* data/
 * data in .csv file
 * sometimes also excel file
 * read.csv(“../data/  “   ) with tab completion to import data file
### doc/
* data management [http://www.britishecologicalsociety.org/wp-content/uploads/Publ_Data-Management-Booklet.pdf]
* data creation
  * data description = meta-data
  * data process (potentially in addition to analysis file)
* report(s) to share with collaborators/advisors
### figs/
* important figures
* sharing with collaborators/advisors
* publication figures
### output/
* copy-paste from console
* model output
* p-values
## R style guide
* script file = where everything happens
  * plain text => readable by anybody
  * easy to save
  * easy to repeat
  * easy to document
  * try to avoid going back to a spreadsheet to process the data
   * one exception: if errors are detected during data processing
* e.g. from Google [https://google.github.io/styleguide/Rguide.xml], some points from that guide
  * spacing
  * commenting
    * why you do something
    * how you do it
    * todo’s
    * data process decisions
    * Structure in your code (see code hierarchy below)
* attach: avoid using it
* use common sense and BE CONSISTENT

## R - studio
* 4 standard windows
  * script file = all the necessary code
   * should be able to run line-by-line to repeat whole analysis
  * console = output
   * try code, but if final solution
 * copy-paste to script file
		* or use history window
* tab completion => you can use descriptive (longer) file names
* soft-wrap R source files (preferences > Code editing) => no need to scroll left-right

### code hierarchy and sections

* # * Heading 1 --------
  * # ** Subheading 1.1 ----------
    * # *** subsub heading 1.1.1 -------------
* any command line with 4 trailing dashes (-) , equal signs (=), or pound signs (#)
* you can fold the code to hide lines that you are not working on
* to navigate between code sections, use “Jump To” menu available at bottom of the editor

## Ultimate goal
* create zip file of your project folder
* send it to somebody else
* naive intelligent observer should be able to repeat the whole analysis
* understand every step of the way


![humor](http://imgs.xkcd.com/comics/code_quality_2.png)
