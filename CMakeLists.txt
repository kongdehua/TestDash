CMAKE_MINIMUM_REQUIRED(VERSION 2.4)
PROJECT(CDashTest)

#-----------------------------------------------------------------------------
# Configure Dart testing support.  This should be done before any
# MESSAGE(FATAL_ERROR ...) commands are invoked.
INCLUDE(CTest)
ENABLE_TESTING()
IF(BUILD_TESTING)
  SET(BUILDNAME "${BUILDNAME}" CACHE STRING "Name of build on the dashboard")
  MARK_AS_ADVANCED(BUILDNAME)
ENDIF(BUILD_TESTING)

# Add a simple test
ADD_TEST(CDashTest1 CDashTest CDashTest) 
ADD_EXECUTABLE(CDashTest main.cxx)
