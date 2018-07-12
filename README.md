# CensusDataframe

Read and clean up census data for a useful data frame

What a total nightmare. The same data from multiple years - the filenames change. The number of layers in the file changes. The field names change. What is wrong with these people?

Files downloaded from:

https://www2.census.gov/geo/tiger/TIGER_DP/

These are the downloaded files (note the change in filename, sigh)

2010_ACS_5YR_BG_48.gdb.zip<br>
2011_ACS_5YR_BG_48.gdb.zip<br>
ACS_2012_5YR_BG_48.gdb.zip<br>
ACS_2013_5YR_BG_48.gdb.zip<br>
ACS_2014_5YR_BG_48.gdb.zip<br>
ACS_2015_5YR_BG_48.gdb.zip<br>
ACS_2016_5YR_BG_48.gdb.zip<br>

Layers in the files:

###-------------------------------------
2010_ACS_5YR_BG_48.gdb.zip
              layer_name geometry_type features fields
1 ACS_10_5YR_BG_48_TEXAS Multi Polygon    15811   1865
2          METADATA_2010            NA      627      2

--->  First few fields are COUNTYFP10, TRACTCE10, BLKGRPCE10 instead of COUNTYFP, TRACTCE, BLKGRPCE
###-------------------------------------
2011_ACS_5YR_BG_48.gdb.zip
              layer_name geometry_type features fields
1          METADATA_2011            NA     1876      2
2 ACS_11_5YR_BG_48_TEXAS Multi Polygon    15811   1880
###-------------------------------------
ACS_2012_5YR_BG_48.gdb.zip
                            layer_name geometry_type features fields  Fields I want to extract
1                           X00_COUNTS            NA    15811      5 
2                      X01_AGE_AND_SEX            NA    15811    107 B01002e1, B01002e2, B01002e3
3                             X02_RACE            NA    15811     71 B02001e1, B02001e2, B02001e3, B02001e4, B02001e5
4        X03_HISPANIC_OR_LATINO_ORIGIN            NA    15811     49 B03002e12
5                        X08_COMMUTING            NA    15811    581
6  X09_CHILDREN_HOUSEHOLD_RELATIONSHIP            NA    15811    175
7     X11_HOUSEHOLD_FAMILY_SUBFAMILIES            NA    15811    281
8       X12_MARITAL_STATUS_AND_HISTORY            NA    15811     39
9                X14_SCHOOL_ENROLLMENT            NA    15811    237
10          X15_EDUCATIONAL_ATTAINMENT            NA    15811    121
11         X16_LANGUAGE_SPOKEN_AT_HOME            NA    15811    164
12                         X17_POVERTY            NA    15811    297
13                          X19_INCOME            NA    15811    349 B19013e1
14                        X20_EARNINGS            NA    15811    107
15                  X21_VETERAN_STATUS            NA    15811    173
16                     X22_FOOD_STAMPS            NA    15811     15
17               X23_EMPLOYMENT_STATUS            NA    15811    539
18             X24_INDUSTRY_OCCUPATION            NA    15811    499
19         X25_HOUSING_CHARACTERISTICS            NA    15811   1689
20            ACS_2012_5YR_BG_48_TEXAS Multi Polygon    15811     15 COUNTYFP, TRACTCE, BLKGRPCE
21                    BG_METADATA_2012            NA     5478      2
###-------------------------------------
###-------------------------------------
###-------------------------------------
###-------------------------------------
###-------------------------------------
###-------------------------------------
###-------------------------------------
