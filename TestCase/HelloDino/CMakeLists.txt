SET(APP_NAME hello_dino)

AUX_SOURCE_DIRECTORY(. hello_dino_src)

ADD_EXECUTABLE(${APP_NAME}
  ${hello_dino_src}
  )

TARGET_LINK_LIBRARIES(${APP_NAME}

  ${LIBRARY_OUTPUT_PATH}/libutility_elastic.a
  ${LIBRARY_OUTPUT_PATH}/libutility_math.a
  ${LIBRARY_OUTPUT_PATH}/libutility_common.a

  libboost_filesystem.so
  libboost_system.so
)