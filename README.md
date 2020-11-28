RaspberryPi project for driving Christmas lights.

## Prerequisites

### [WiringPi](http://wiringpi.com/)

    sudo apt install wiringpi

### [Boost](www.boost.org)

#### Building Boost

Create `~/user-config.jam` containing the following:

    using gcc : c++17 : "g++" : <cxxflags>-std=c++17 ;

Download and extract Boost. From the Boost root directory, run

    ./bootstrap.sh --prefix=/usr/local
    sudo ./b2 -q variant=release link=shared runtime-link=shared threading=multi toolset=gcc cxxflags="-std=c++17 -march=native" install
