SET(LIBRARY_NAME utility_common)
AUX_SOURCE_DIRECTORY(. common_src)

ADD_LIBRARY(${LIBRARY_NAME} 
  ${common_src}
)