<!--
Add here global page variables to use throughout your
website.
The website_* must be defined for the RSS to work
-->
@def website_title = "Sen Yang"
@def website_descr = "An interesting place."
@def website_url   = ""

@def author = "Yang Sen"

@def mintoclevel = 2

<!--
Add here files or directories that should be ignored by Franklin, otherwise
these files might be copied and, if markdown, processed by Franklin which
you might not want. Indicate directories by ending the name with a `/`.
-->
@def ignore = ["node_modules/", "franklin", "franklin.pub"]

<!--
Add here global latex commands to use throughout your
pages. It can be math commands but does not need to be.
For instance:
* \newcommand{\phrase}{This is a long phrase to copy.}
-->
\newcommand{\definition}[2]{
  @@definition
  **Definition**: (_!#1_)
  #2
  @@
}

\newcommand{\example}[1]{
  @@example
  **Example**: #1
  @@
}

\newcommand{\important}[1]{
    @@important
    #1
    @@
}

\newcommand{\bluebox}[1]{
    @@colbox-blue
    #1
    @@
}

