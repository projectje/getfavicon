# getfaviconsfromdirs
Parses a folderstructure with text files and downloads a favicon for each url found in them from the Google Favicon service.

This can be used for pre-caching during/before build for these icons or for retrieving just a set of application icons

# install

npm i getfaviconsfromdirs

# usage

pass the folder to read and the folder to write icons to, to the function "getFavicon"

# example

`
getFavicon('c:/a/website//src/assets/data/', 'c:/a/websites/icon/');
`

or e.g. in package.json before build:

`
"scripts": {
    "fetchicons": "run-func /src/util/favicon.js getFavicon c:/a/website//src/assets/data/ c:/a/websites/icon/"
  }
`
# runtime

During runtime you can reference the icons by following the same logic to build the url:

const imgFilePath = imgRootDir + url.split("/")[2].split('.').reverse().join('/') + "/favicon.png";
