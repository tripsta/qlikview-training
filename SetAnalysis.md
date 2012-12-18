
Set Analysis
=============

The following code is an expression that gets the selected year's sales
sum({$<Year={$(=Only(year))}>} Sales)

The following code is an expression that gets the selected year's sales
sum({$<Year={$(=Only(year)-1)}>} Sales)

The following code (0 instead of $) is an expression that gets the selected year's sales, however ignores any other user selection inthe results.
sum({0<Year={$(=Only(year))}>} Sales)

$ or $0 current Selection
1 -> full

following options are used to navigate with back and forward to exluce/include last clicked filters
$1 -> back
$_1 -> forward

Bookmark when user has created a bookmark with selection criteria that should be loaded.
BM01 -> BookmarkID  
Bookmark -> BookmarkName
sum({MyBookmark<Year={$(=Only(year))}>} Sales)
if bookmark contains multiple years, developer setting takes precedence

{1-$} -> exluded  //uses exclusion operator. all filters other than user selection


Set Operators
=============
+ Union (all A and all B.. might have duplicates
- Exclusion  (all A - B)
* Intersection (common elements on A and B)
/ Symmetric Difference (all - intersection)


Modifier Described
========
modifier everything between <>
<.........> 
<Year={'2012'}>
<Year={'2012', '2011'}>
<Year={'2012'}, Region={'GR'}>

<Year={$(vCurrentYear)}>  // uses variable
