# PPTs
Precipitation Processing Tools (PPTs) it's an open source code developed by Vinícius Mesquita to download and process satellite precipitation data from NASA Tropical Rainfall Measuring Mission (TRMM) and Global Precipitation Measurement Mission (GPM)

Requisites:

  * Python 3.6 or above
  
  * PyQt5 python package
  
  * Gdal python package and Gdal Binaries (if Unix system)
  
  * **WGET package** (If windows!, download Cygwin setup here http://cygwin.com/install.html, install with wget package and add C:\cygwin64\bin to variables of the system) - Tutorial: http://www.bloggingtips.info/install-wget-windows/. __Don't forget to add Cygwin (C:\cygwin64\bin) to the systen vauable PATH__
  
  
Recommendations: 
   * Install Anaconda Python 3.6 or above (https://www.anaconda.com/download/) and the Gdal package (https://anaconda.org/conda-forge/gdal) and, for Windows users, add some system variables like:
     * PATH =  C:\ProgramData\Miniconda3; C:\ProgramData\Miniconda3\Library\bin; C:\ProgramData\Miniconda3\Scripts;
     * GDAL_DATA = C:\ProgramData\Miniconda3\Library\share\gdal
   * Before you try to download the data, create an account in NASA EartData website (https://urs.earthdata.nasa.gov), make login, click in Applications>Authorized Apps> Approve More Applications and select ***NASA GESDISC DATA ARCHIVE***.

# HOW TO RUN

You can use the **PPT_UI_RUN.py** to run an user-friendly interface or parse some arguments to ***Integration.py*** like:


***--ProdTP*** = 'GPM_M','GPM_D','TRMM_M','TRMM_D'

GPM_M: GPM Monthly (IMERGM v4)

GPM_D: GPM Daily (IMERGDF v4)

TRMM_M: TRMM Monthly (TRMM 3B43 v7)

TRMM_D: TRMM Daily (TRMM 3B42 v7)

***--StartDate*** = Insert the start date

***--EndDate*** = Insert the end date

***--ProcessDir*** = Insert the processing directory path

***--SptSlc*** = Insert the slice feature path (if not used, it assumes a Global product)

***--OP*** = Call this argument if you wanna Only Process the data. Make sure you have a directory with a raw files subfolder!!!!
 
 
 **E.G.***: python Integration.py --ProdTP GPM_M --StartDate 2018-01-01 --EndDate 2018-12-31 --ProcessDir ~./mydirectory --SptSlc ~./brazil_boundary.shp --OP
 
 
 ***UNDER CONSTRUCTION!***
 You may experience bugs and prints in brazilian portuguese
 
 
