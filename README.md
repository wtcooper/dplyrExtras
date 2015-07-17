# dplyrStrWrap
Simple wrappers from Sebastian Kranz (gist.github.com/skranz/9681509) in package form to ease install across machines.  Allows one to pass column names to most dplyr methods, where method name is of the form s_methodName().  

E.g., instead of the following existing approach:

dots <- lapply(colNameAsString, as.symbol)
df %>% group_by_(.dots=dots)

One would use:

df %>% s_group_by(colNameAsString)

Other approaches exist when working with strings for column names in dplyr, but this may be a more natural feel for many users.
