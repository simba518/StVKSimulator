SET(LIBRARY_NAME utility_elastic)
AUX_SOURCE_DIRECTORY(. elastic_src)

ADD_LIBRARY(${LIBRARY_NAME}
  ${elastic_src}
)