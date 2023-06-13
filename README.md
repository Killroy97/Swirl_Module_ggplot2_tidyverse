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
- [Contributing](#contributing)
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

To install the package. Navigate to [project_files](Linkhere) 
The contents of this module can be found on this Github repository. Please make sure you are well connected to the Internet to download all the necessary files. The following files can be found and are necessary to run the entire module: 1. lesson.yaml 2. initLesson.R 3. dependson.txt 4. customTests.R  

Once the user has downloaded the .swc file from the repository, They can simply use the command
```
library(swirl)
swirl::install_course_directory(filepath)
```
The user has now successfully installed the course!Now, to begin the course, the user can simply run
```
swirl()
```
Running the above code will provide the user with the course menu.

**NOTE**: The course module “facets and Geometric objects” requires installed R packages before you could
install the course. An R package is a group of additional functions, information, and documentation for the
R programming language.  

**Pre-requsites**: The following packages are required before running the package.   
1. Tidyverse 
```
install.packages("tidyverse")
```
2. World bank data to import the datset used in this course 
```
install.packages("WDI")
```
3. Pacman
```
install.packages("pacman")
```
Once all the required packages are installed. The following datasets can be imported directly into the global environment by:

```
urbanpopulation= WDI(indicator= "SP.URB.TOTL", country = c('AU','BR','CN','DE','IN','NG','US'),
start =1990, end = 2020 )
```
```
forestarea= WDI(indicator= "AG.LND.FRST.K2", country = c('AU','BR','CN','DE','IN','NG','US'),
start =1990, end = 2020 )
```
**What datasets are choosen and why?**
The first data set selected from the world bank data was Urban population growth in the
world. Since the data set consisted of all the countries in the world, we wanted to narrow it down to
one country from each part of the world, which resulted in the data of 7 countries.
The second data set chosen was the Forest land (in sq.km) of the same countries as the first data set.
The reason behind choosing this data set was that we wanted to highlight the correlation between growing population and declining forest area as we see it.  

## Usage
Once the installation of different libraries and datasets are done, the individual can start learning the course by simply following the instructions presented on the console. Any hurdles can be overcome by simply accessing the hint, or the examplar answer by procceding further.
 

## Contributing

We welcome contributions from the community! If you would like to contribute to this project, please follow these guidelines:

1. Fork the repository and create your branch: `git checkout -b feature/YourFeature`
2. Commit your changes: `git commit -am 'Add some feature'`
3. Push to your branch: `git push origin feature/YourFeature`
4. Create a pull request describing your changes.

Please ensure that you adhere to the project's coding conventions, documentation guidelines, and code of conduct.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

If you have any questions, suggestions, or feedback, please feel free to reach out to us:

- Project Website: [example.com](https://example.com)
- Project Issues: [GitHub Issues](https://github.com/yourusername/yourrepository/issues)
- Email: your-email@example.com
- Twitter: [@yourtwitterhandle](https://twitter.com/yourtwitterhandle)





