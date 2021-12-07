include(${CMAKE_CURRENT_SOURCE_DIR}/../../max-sdk-base/script/max-pretarget.cmake)

include_directories(
    "${MAX_SDK_INCLUDES}"
    "${MAX_SDK_MSP_INCLUDES}"
    "${MAX_SDK_JIT_INCLUDES}"
    "${CMAKE_CURRENT_SOURCE_DIR}"
)

add_library(
    ${PROJECT_NAME}
    MODULE
        ${CMAKE_CURRENT_SOURCE_DIR}/fft_mayer.proto.h
        ${CMAKE_CURRENT_SOURCE_DIR}/trigtbl.h
        ${CMAKE_CURRENT_SOURCE_DIR}/fft_mayer.c
        ${CMAKE_CURRENT_SOURCE_DIR}/fiddle~.c
)

include(${CMAKE_CURRENT_SOURCE_DIR}/../../max-sdk-base/script/max-posttarget.cmake)
