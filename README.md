# Swirl Course: Data Visualization with ggplot2  

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)  

Learning R programming can be greatly enhanced through data visualization, which offers elegant and informative plots that facilitate quick analysis and comprehension of data frames. To provide users with an interactive and practical learning experience in R programming, I have developed a swirl package that transforms the R console into an engaging learning environment.

This swirl course focuses specifically on teaching users data visualization using the popular ggplot2 package. Divided into three modules, each module covers different aspects of data visualization methods: scatter plots, facets and geometric objects, and bar graphs. The course is designed to guide users step-by-step, allowing them to learn at their own pace and grasp each aspect of the data visualization process.

By completing these modules, users will gain the ability to write appropriate code, understand the underlying process, and effectively implement data visualization techniques. With this newfound knowledge, users will be equipped to leverage data visualization for strategic decision-making, making it easier and faster to derive insights from their data.

Please note that a basic understanding of R and RStudio is expected in order to fully grasp the concepts presented in this course.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Contact](#contact)

## Features

1. **Interactive Learning Environment:** The swirl package converts the R console into an interactive learning environment, allowing users to learn data visualization in a hands-on and engaging manner.  

2. **Focused on ggplot2:** The course specifically emphasizes the use of the ggplot2 package, which is widely recognized for its powerful and flexible data visualization capabilities in R.  

3. **Modular Structure:** The course is divided into three modules, each covering different data visualization methods: scatter plots, facets and geometric objects, and bar graphs. This modular structure enables users to focus on specific visualization techniques as per their needs.  

4. **Step-by-Step Guidance:** Each module provides step-by-step instructions and exercises, helping users understand and apply various aspects of the data visualization process. This approach ensures a thorough understanding of the concepts and techniques involved.  

5. **Self-Paced Learning:** The swirl course allows users to learn at their own pace, giving them the flexibility to revisit concepts and exercises as needed. This self-paced learning approach accommodates users with varying levels of experience and ensures a comfortable learning experience.  

6. **Practical Applications:** The course emphasizes the practical application of data visualization for strategic decision-making. Users will learn how to analyze and present data effectively, enabling them to make informed decisions based on visual insights.  

7. **Assumes Basic R Knowledge:** To fully comprehend the course material, a basic understanding of R and RStudio is expected. Users should be familiar with R syntax and data manipulation concepts.  


## Installation

To install the package. Navigate to [project_files](facets_and_geometric_objects) 
The contents of this module can be found on this Github repository. Please make sure you are well connected to the Internet to download all the necessary files. The following files can be found and are necessary to run the entire module: 1. lesson.yaml 2. initLesson.R 3. dependson.txt 4. customTests.R  

**Pre-requsites**: The following packages are required before running the package.   
1. Tidyverse 
```ruby
install.packages("tidyverse")
```
2. World bank data to import the datset used in this course 
```ruby
install.packages("WDI")
```
3. Pacman
```ruby
install.packages("pacman")
```
Once all the required packages are installed. The following datasets can be imported directly into the global environment by:

```ruby
urbanpopulation= WDI(indicator= "SP.URB.TOTL", country = c('AU','BR','CN','DE','IN','NG','US'),
start =1990, end = 2020 )
```
![Dataset_1](https://github.com/Killroy97/Swirl_Module_ggplot2_tidyverse/assets/132211845/ed3d50bd-8999-47b7-8e7f-4ac625cc6308)  

```ruby
forestarea= WDI(indicator= "AG.LND.FRST.K2", country = c('AU','BR','CN','DE','IN','NG','US'),
start =1990, end = 2020 )
```
![Dataset_2](https://github.com/Killroy97/Swirl_Module_ggplot2_tidyverse/assets/132211845/90e7ef00-0ad3-4d60-8283-9d87ba2c9b7f)  

Subsequently, the usage of merger function by entering the following code will provide us with the master data required to go ahead with this course module.
```ruby
master_data = merge(urbanpopulation, forestarea, by = c("iso2c","year", "country"))
```
![Global_environment](https://github.com/Killroy97/Swirl_Module_ggplot2_tidyverse/assets/132211845/c7f80fa9-7de4-4924-bd90-8dffb3a95a14)  
![Master_data](https://github.com/Killroy97/Swirl_Module_ggplot2_tidyverse/assets/132211845/cb0fef00-3c07-40fb-945e-8b09e19e1377)  

Column names can be changed according to desire, thus making the data frame more readable.This can be
done using the colnames function.
```ruby
colnames(dataframe)[which(names(dataframe) == "columnName")] <- "newColumnName"
```
![Column_names_updated](https://github.com/Killroy97/Swirl_Module_ggplot2_tidyverse/assets/132211845/a7dad0f6-f568-4f96-9a1d-fe9eb0ad1110)  


**What datasets are choosen and why?**
The first data set selected from the world bank data was Urban population growth in the
world. Since the data set consisted of all the countries in the world, we wanted to narrow it down to
one country from each part of the world, which resulted in the data of 7 countries.
The second data set chosen was the Forest land (in sq.km) of the same countries as the first data set.
The reason behind choosing this data set was that we wanted to highlight the correlation between growing population and declining forest area as we see it.

Once the user has downloaded the .swc file from the repository, They can simply use the command
```ruby
library(swirl)
swirl::install_course_directory(filepath)
```
The user has now successfully installed the course!Now, to begin the course, the user can simply run
```ruby
swirl()
```
Running the above code will provide the user with the course menu.

**NOTE**: The course module “facets and Geometric objects” requires installed R packages before you could
install the course. An R package is a group of additional functions, information, and documentation for the
R programming language.    

## Usage
- Once the installation of different libraries and datasets are done, the individual can start learning the course by simply following the instructions presented on the console. Any hurdles can be overcome by simply accessing the hint, or the examplar answer by procceding further.  

- The course module will take the learner through a inteactive learning environment where they can test their knowledge about R codes and test them. 
- The individual will be able to understand the process to creating optimal geometry and facets for any datset desired by the end of this course. 
- The [Project Report] (Project Report.pdf) can be used to navigate through the course, and also acts as a project report. 


Please ensure that you adhere to the project's coding conventions, documentation guidelines, and code of conduct.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

If you have any questions, suggestions, or feedback, please feel free to reach out to us:

- Project Issues: [GitHub Issues](https://github.com/yourusername/yourrepository/issues)
- Email: srikarmulgund97@gmail.com






