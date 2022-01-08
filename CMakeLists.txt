add_library(vl53l0x INTERFACE)

target_include_directories(vl53l0x INTERFACE
        ${CMAKE_CURRENT_LIST_DIR}/core/inc
        ${CMAKE_CURRENT_LIST_DIR}/platform/inc
)

target_sources(vl53l0x INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/core/src/vl53l0x_api.c
	${CMAKE_CURRENT_LIST_DIR}/core/src/vl53l0x_api_calibration.c
	${CMAKE_CURRENT_LIST_DIR}/core/src/vl53l0x_api_core.c
	${CMAKE_CURRENT_LIST_DIR}/core/src/vl53l0x_api_ranging.c
	${CMAKE_CURRENT_LIST_DIR}/core/src/vl53l0x_api_strings.c
)

target_link_libraries(vl53l0x INTERFACE pico_stdlib hardware_i2c)
