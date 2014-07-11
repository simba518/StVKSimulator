SET(LIBRARY_NAME utility_math)
AUX_SOURCE_DIRECTORY(. math_src)

ADD_LIBRARY(${LIBRARY_NAME} 
  ${math_src}
)