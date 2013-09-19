
project(features)

file(
	GLOB_RECURSE
	features_files
	*.hpp
)
			
set_source_files_properties(${features_files} PROPERTIES LANGUAGE CXX)

INSTALL(DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}"
    DESTINATION include/openMVG
    FILES_MATCHING PATTERN "*.hpp"
    PATTERN "*_test.*" EXCLUDE)

UNIT_TEST(openMVG features "")

