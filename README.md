# getfavicon
Parses a folderstructure with text files and downloads a favicon for each url found in them from the Google Favicon service.

This can be used for pre-caching these icons.

# usage

pass the folder to read and the folder to write icons to, to the function "TraverseDir"

# example

`
TraverseDir('c:/a/website//src/assets/data/', 'c:/a/websites/icon/');
`

or e.g. in package.json before build:

`
"scripts": {
    "fetchicons": "run-func /src/util/favicon.js TraverseDir c:/a/website//src/assets/data/ c:/a/websites/icon/"
  }
`
