# MSDS-6306-Homework
Homework :
Assignment 4 

Introduction: 

In this assignment we are learning to webscrap data from 2 different websites. The first quesitons we will sort the information pulled from the website IMDb and build a table. The 2nd question we will obtain a table and draw a graph of the Spurs players and their field goal percentage. Overall, the Spurs graph demonstrates the Point Forward (PF) has the highest field goal percentage. 

SessionInfo:

R version 3.5.1 (2018-07-02)
Platform: x86_64-apple-darwin15.6.0 (64-bit)
Running under: macOS Sierra 10.12.6

Matrix products: default
BLAS: /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libBLAS.dylib
LAPACK: /Library/Frameworks/R.framework/Versions/3.5/Resources/lib/libRlapack.dylib

locale:
[1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] tidyr_0.8.2     rvest_0.3.2     xml2_1.2.0      stringr_1.3.1   imdbapi_0.1.0   RCurl_1.95-4.11 bitops_1.0-6   
 [8] RJSONIO_1.3-1.1 jsonlite_1.6    XML_3.98-1.16  

loaded via a namespace (and not attached):
 [1] Rcpp_1.0.0       pillar_1.3.1     compiler_3.5.1   bindr_0.1.1      tools_3.5.1      digest_0.6.18   
 [7] evaluate_0.12    tibble_1.4.2     pkgconfig_2.0.2  rlang_0.3.1      rstudioapi_0.9.0 curl_3.2        
[13] yaml_2.2.0       xfun_0.4         bindrcpp_0.2.2   dplyr_0.7.8      httr_1.4.0       knitr_1.21      
[19] tidyselect_0.2.5 glue_1.3.0       R6_2.3.0         rmarkdown_1.11   purrr_0.3.0      selectr_0.4-1   
[25] magrittr_1.5     htmltools_0.3.6  rsconnect_0.8.13 assertthat_0.2.0 stringi_1.2.4    crayon_1.3.4 


Contribution: 

Website: http://www.imdb.com/title/tt1201607/fullcredits?ref_=tt_ql_1  IMDb.com, Inc., 02 February 2019. 

Website: http://www.espn.com/nba/team/stats/_/name/sa/san-antonio-spurs, ESPN, Inc., 545 Middle St, Bristol, CT 06010, 02 February 2019. 



Questions: 
	
1. Harry Potter Cast :  
	a. In the IMDB, there are listings of full cast members for movies. Navigate to http://www.imdb.com/title/tt1201607/fullcredits?ref_=tt_ql_1. Feel free to View Source to get a good idea of what the page looks like in code. 
	b. Scrape the page with any R package that makes things easy for you. Of particular interest is the table of the Cast in order of crediting. Please scrape this table (you might have to fish it out of several of the tables from the page) and make it a data.frame() of the Cast in your R environment 
	c. Clean up the table 
	• It should not have blank observations or rows, a row that should be column names, or just ‘…’ 
	• It should have intuitive column names (ideally 2 to start – Actor and Character) 
	• In the film, Mr. Warwick plays two characters, which makes his row look a little weird. Please replace his character column with just “Griphook / Professor Filius Flitwick” to make it look better. 
	• One row might result in “Rest of cast listed alphabetically” – remove this observation. 
	
	d. Split the Actor’s name into two columns: FirstName and Surname. Keep in mind that some actors/actresses have middle names as well. Please make sure that the middle names are in the FirstName column, in addition to the first name (example: given the Actor Frank Jeffrey Stevenson, the FirstName column would say “Frank Jeffrey.”) 

	e. Present the first 10 rows of the data.frame() – It should have only FirstName, Surname, and Character columns. 
2. SportsBall :
	a. On the ESPN website, there are statistics of each NBA player. Navigate to the San Antonio Spurs current statistics (likely http://www.espn.com/nba/team/stats/_/name/sa/san-antonio-spurs). You are interested in the Shooting Statistics table. 
	b. Scrape the page with any R package that makes things easy for you. There are a few tables on the page, so make sure you are targeting specifically the Shooting Statistics table. 
c. Clean up the table (You might get some warnings if you’re working with tibbles) 
• You’ll want to create an R data.frame() with one observation for each player. Make sure that you do not accidentally include blank rows, a row of column names, or the Totals row in the table as observations. 
	• The column PLAYER has two variables of interest in it: the player’s name and their position, denoted by 1-2 letters after their name. Split the cells into two columns, one with Name and the other Position. 
	• Check the data type of all columns. Convert relevant columns to numeric. Check the data type of all columns again to confirm that they have changed! 
	
d. Create a colorful bar chart that shows the Field Goals Percentage Per Game for each person. It will be graded on the following criteria. 
• Informative Title, centered 
	• Relevant x and y axis labels (not simply variables names!) 
	• Human-readable axes with no overlap (you might have to flip x and y to fix that). Note: You do not have to convert the decimal to a percentage. 
	• Color the columns by the team member’s position (so, all PF’s should have the same color, etc.) 
	
	

