Direct Demod - Automatic NOAA Map and Globe Projection
======================================================

Combining Maps from Multiple DSGN Stations and Scrolling through Time
---------------------------------------------------------------------

### This project is for adding supplement files for the following [proposal](https://docs.google.com/document/d/1dH36BWyLU2bjtMudt8bBVoROjMZty47-XSv6j485FmY/edit?usp=sharing).

### Contents

This project aims to improve the current rendering of map and globe from DirectDemod python libraries, along with combining maps from different stations and being able to view data along a large time-zone.

The following issues are faced while rendering data from multiple record stations, combining and syncing them, along with rendering them -

*   **Large Data Set**  
    The data set to be represented for this project is very large. Having data from many satellites, and having many captures of data from each satellite per day, leads us to the problem of maintaining and handling large data sets. We have to cover obtaining data from DSGN stations, and their parallel processing using python script.
  
*   **Efficient Data Retrieval**  
    Efficient Data Retrieval from data-bases is also important for faster rendering of data into web-page. We have to design our database schema in such format, that we have both write and retieve operation as fast as possible, i.e.  
    1\. when processing data, we can store it efficiently  
    2\. accesing data for rendering  
    For this, we will use the concept of de-centralised NoSQL database. The schema is discussed below.
  
*   **Algorithm for merging and syncing of processed data**  
    As we are showing data through time, we will collect the data, over a large range of days, from many satellites.There is a good possibility that data from the satellites are captured at differnet timestamps, and we need to devise an algorithm, to sync and merge the data captured at different time.
  
*   **Merging of Different Data Sets**  
    The merge python code, as worked on during last summer, will need modification, as now we are merging data-sets over an added parameter - time.
  
*   **Time Scrolling**  
    Discussed as .gif format below.
  
*   **Increase Robustness**  
    A new data-format, offset variable is added to help improve the robustness of the webpage, and increase user flexibility.