cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
    URL "https://github.com/lsolanka/hunter/archive/4ecf66e071495981031fdfa99aad576405537266.tar.gz"
    SHA1 "d4495d186db78814578908e3835cbfc15b9429b7"
)

project(cmake_modules)
hunter_add_package(catkin)

find_package(catkin REQUIRED)

catkin_package(CFG_EXTRAS cmake_modules-extras.cmake)

## Install all cmake files
install(DIRECTORY cmake/Modules
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/cmake)
