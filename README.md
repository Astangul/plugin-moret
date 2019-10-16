[![Build Status](https://travis-ci.org/Funz/plugin-MORET5.png)](https://travis-ci.org/Funz/plugin-MORET5)

# Funz plugin: MORET5

This plugin is dedicated to launch MORET5 calculations from Funz.
It supports the following syntax and features:

  * Input
    * file type supported: '*.MORET5', any other format for resources
    * parameter syntax: 
      * variable syntax: `$(...)`
      * formula syntax: `@{...}`
      * comment char: `*`
    * example input file:
        ```
        ...
        ... $(x1~[1,2]) ...
        ... $x1 ...
        ...
        ```
      * will identify input:
        * x1, expected to vary inside [1,2]
        * x2, expected to vary inside [0,1] (by default)
      * replace `!{?x2 + 1.23 | #.###}` expression by its evaluation

  * Output
    * file type supported: '*.MORET5.out'
    * read any named value printed with `=`, like `...`
    * example output file:
        ```
        ...
        z= ...
        ...
        ```
        * will return output:
          * z=... 


![Analytics](https://ga-beacon.appspot.com/UA-109580-20/plugin-MORET5)
