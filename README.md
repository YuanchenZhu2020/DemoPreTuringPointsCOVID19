
<!-- README.md is generated from README.Rmd. Please edit that file -->

# DemoPreTurningPointsCOVID19

<!-- badges: start -->

<!-- badges: end -->

This R package aims to implementing the computational framework in the
paper *[Tracking and forecasting milepost moments of the epidemic in the
early outbreak framework and applications to the
COVID-19](https://www.medrxiv.org/content/10.1101/2020.03.21.20040139v1.full.pdf+html)*
based entirly on the [Vicky-Zh’s
work](https://github.com/Vicky-Zh/Tracking_and_forecasting_milepost_moments_of_COVID-19.git).

## Installation

You can install it as a source code package or binary package.

Install from source code:

  - download and install RTools:
    <https://mirrors.tuna.tsinghua.edu.cn/CRAN/bin/windows/Rtools/>
  - install devtools in R `install.packages("devtools")`
  - install packages in R
    `devtools::install_github("YuanchenZhu2020/DemoPreTurningPointsCOVID19")`

Install from binary file:

  - Download Binary File :
    <https://bhpan.buaa.edu.cn:443/link/DB80C0730C36DA9384524893CD143796>
  - Get the path of this binary file `pkgfilepath`
  - Install packages in R `install.packages(pkgfilepath, repos = NULL,
    type = "win.binary")`

<!-- end list -->

``` r
# install as a source code package (requires RTools)
# install.packages("devtools")
devtools::install_github("YuanchenZhu2020/DemoPreTurningPointsCOVID19")

# install as a binary package.
# 1. download binary package to your PC
# 2. get the path of package file
install.packages(pkgfilepath, repos = NULL, type = "win.binary")
```

## Usage

FUnction List:

  - get\_indicators
  - calc\_velocity
  - get\_future\_indicators
  - corr\_removed\_rate
  - get\_milepost
  - prediction
  - period\_predict

Dataset List:

  - COVID19\_CN

If you want to see details of each function, use `help(name)`.

## Example

``` r
library(DemoPreTurningPointsCOVID19)
# single begining time
single_result <- prediction(COVID19_CN, M = 5, Begining_Time = "2020-01-29")

# multiple begining time
period_result <- period_predict(COVID19_CN, M = 5, Begining_Time = "2020-01-29", period = 32)
```
