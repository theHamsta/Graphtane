file(GLOB CoreFiles *.cpp *.h)

set(SourceFiles ${CoreFiles})

SOURCE_GROUP("Source Files" FILES ${CoreFiles})

include_directories(..)

find_package(GVis)
include_directories(${GVis_INCLUDE_DIRS})

add_library(GSparseVolumes ${Graphtane_LIB_TYPE} ${SourceFiles})

target_link_libraries (GSparseVolumes ${GVis_LIBRARIES})