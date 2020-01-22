## Day 3 - Preparing data for analysis

### Cleaning a data table

_For this excercise, I chose the following dataset: '395 - Snow, Hail, Ice 
Pellets, and Sleet--Selected Cities'. The table already appeared quite clean
to me, hence I applied minor edits. I got rid of the rows where the annual records
of snow, hail, ice pellets and sleet was zero, and merged the first to columns
and removed the top and bottom rows so that there are no cells with redundant
information, and that the focus is on the values._

- First the last column was moved to the beginning to have it next to the flags, 
using the **‘Edit column’** and **‘Move column to beginning’** options. 

- The rows with an annual record of 0 were flagged, in addition to the rows with 
footnotes (these rows were on the second page, as there were more than 50 rows). 
They were then removed from the table through **‘Facet by flag’**, and then 
**include** only the records that are **‘false’**. 8 rows were thus deleted. 

- The column showing the annual records was then moved to the end again. 

- For the records where the state was missing, the state was added manually 
using the **‘edit’** option in the cell.

- The first column was renamed to ‘Column 1’, through **‘Edit column’** and **‘Rename 
this column’**. 

- A new column was then made through **‘Add column based on this column’**.  In the 
**Expression box**, the following was written: 
  > cells['Column 1'].value+ '- ' + cells['Column 2'].value. 

  The new column was named "State and station".

- This was then undone by pressing **‘Undo’**, and the columns were then merged in _another 
way_. Under Column 1, I selected the option **‘Join columns’**, then selected Column 1 
and Column 2, wrote ‘- ‘ as the **separator** and selected **‘Delete joined columns’**.

- The table was then exported to a csv file. 

#### Data source
The data table was obtained from the United States Census Bureau, [Section 6. Geography and Environment (2012).](https://www.census.gov/library/publications/2011/compendia/statab/131ed/geography-environment.html "United States Census Bureau")


