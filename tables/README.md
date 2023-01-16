If you feel inclined to add acronyms to the csv file, please note the following: 

The CSV file also serves as an input to a script that automatically creates acronym files for $\LaTeX$ that are compatible with the `glossaries` package. 
This package has a large number of options and provides great flexibility to use the acronyms in a $\LaTeX$ project, so to make the best possible use of 
the acronyms, some ground rules should be followed:

1. The long text for the acronym in the column labeled `Translation` should not start with a capital letter unless it is a proper noun, 
as this makes it cumbersome to use it in a sentence. If you do need the capital letter, you can use the `\Ac{}` command instead of the `\ac{}` command. 
2. `glossaries` provides a large number of possible versions for the acronym, among other things the `\acp{}` command provides an automatic plural version
of the full text. This can lead to a problem, as some English words change their spelling in the plural, ie 'assembly' becomes `assemblies`, not 'assemblys'
This is why the `.CSV` file has a fourth column `options`. The value of this column is taken verbatim into the optional argument of `\newacronym` so that 
you can use the `longplural` option to define the proper plural form.
