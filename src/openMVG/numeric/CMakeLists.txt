ADD_LIBRARY(openMVG_numeric
			numeric.cpp
			numeric.h)

INSTALL(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
    DESTINATION include/openMVG
    FILES_MATCHING PATTERN "*.hpp" PATTERN "*.h"
    PATTERN "*_test.hpp" EXCLUDE)
INSTALL(TARGETS openMVG_numeric ARCHIVE DESTINATION lib)
			
UNIT_TEST(openMVG numeric openMVG_numeric)
UNIT_TEST(openMVG poly openMVG_numeric)
UNIT_TEST(openMVG lm openMVG_numeric)
