    /**************************************************************************************************************************
    ee.Screen.js (y.rytsikau@gmail.com, 2019-03-06)
    Taking Screenshots in JPG/PDF/PNG/TXT(UTF-8) formats for the list of urls
    ***************************************************************************************************************************

    Tested Configuration:
    MS Windows 10 Pro x64 (build 17134), Node.js 10.14.2, Puppeteer 1.11.0

    Dependencies:
    Node.js, Google Chrome Puppeteer
        
    To install Node.js, visit page https://nodejs.org
    To install Puppeteer, after installing Node.js, open Windows command line, and type "npm install --save puppeteer"
    
    Using from command line:
       node "c:\path\to\ee.Screen.js" "c:\path\to\someListWithUrls.anyTextFile"
    If list has name "list.txt", and located in one directory with this script, simply run file "start.bat".
    File "list.txt" must be encoded in UTF-8, format of line is next:
       <url>;"<path>\<to>\<ScreenshotFile>.~~~";width*height;commaSeparatedFormatsToDo
    Order of values in line does not matter. All values except <url> are optional, default values are:
       "<thisScriptDir>\ee.Screen\<flatUrl>.~~~" - for path and filename of screenshot;
       1280*full - for resolution;
       jpg,pdf,png,txt - for formats.
    Screenshots in PDF and TXT saves full document - TXT according to HTML-markup, PDF - to A4 scaled as 100%.
    To make PDF screenshot in landscape orientation, write "Lpdf" instead of "pdf" in the field of need formats.
    If path not specified, screenshots will be saved in "screenshots" directory.
    Existing screenshots are skipped, new ones in that case will not be made.
    
    Example of list' content:
       https://www.google.com/;"C:\My Screenshots\123.~~~";1024*768;jpg,Lpdf
       https://github.com
       txt,pdf;1920*full;https://www.bbc.co.uk/news
    
    **************************************************************************************************************************/
