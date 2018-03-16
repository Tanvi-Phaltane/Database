# Database
A collection of plants, alongwith their chemical compounds, which are experimentally proven to have anti-diabetic property. 

# Prerequisites
WAMP server v3.1.0 for 64-bit Windows machine(Apache v2.4.27 - PHP v5.6.31 - MySQL v5.7.19)

# Installation 
1) Download server from 'https://sourceforge.net/projects/wampserver/'
1) Install the wamp64 server on your local machine by following the software installation steps.
2) Run wampmanager.exe file
3) Right click on WampServer 'W' logo and select 'Localhost' to check successful running of wamp server
4) Create a new folder 'my_final_proj' in 'wamp64/www' local directory.
5) Place the code files in 'my_final_proj'
6) Again, open localhost and check if 'my_final_proj' folder is visible.
7) Click on 'my_final_proj' folder to view list of files


# Usage for local machine
1) Check browser specified in 'wampmanager.conf' file -> navigator attribute.
    eg: In my case, navigator ="C:/Program Files (x86)/Google/Chrome/Application/chrome.exe"
2) Accordingly open the browser and type localhost/my_final_proj/home.html
3) Similarly, you can load other HTML pages by specifying file name in above URL

A) Basic Search:
    1) In order to qurey the database using basic search (basic_search.html), select any one of the fields (Plant name, Comppund              name, Diabetes type, Experimental evidence, Combination therapy) using drop-down menus
    eg: Plant_name = 'Galega officinalis'
    2) After selecting any one field, click on 'Submit' button.
    3) The user will be directed to 'basic_results.php' page displaying entries related to submitted query.

B) Advanced Search:
    1) User can carry out an advanced search (advanced_search.html) based on Plant name  AND Compound name AND Diabetes type.
    2) The user has to select all fields and then click on Submit.
    3) As the query is AND operated, 'advanced_results.php' page displays entries related to submitted query.

C) Upload Data: 
    1) User needs to fill up the form with details such as Name, Email id, Institute Name and Comments(optional).
    2) User can then upload file in the form of Excel sheet (.xls, .xlsx, .tsv, .csv or .txt accepted)
    3) The file should contain following columns in the same order:
    Plant_name, Plant_part, Compound_name, Diabetes_type, Effect, Experimental_method, PubChem_ID, Dose, Reference, Combination_therapy 
    4) After the user has submitted the data, it will be checked by concerned authorities and then incorporated in the database. A confirmation email will be sent to the submitter on incorporation. 
    






