PROJECT(Lab_PWP)

cmake_minimum_required(VERSION 2.4)
if(COMMAND cmake_policy)
  cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

find_package(OpenIGTLink REQUIRED)

include(${OpenIGTLink_USE_FILE})

ADD_EXECUTABLE(NowyKlient   NowyKlient.cxx)
TARGET_LINK_LIBRARIES(NowyKlient OpenIGTLink)

ADD_EXECUTABLE(NowySerwer   NowySerwer.cxx)
TARGET_LINK_LIBRARIES(NowySerwer OpenIGTLink)


