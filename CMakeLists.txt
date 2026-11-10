list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_LIST_DIR}/eil-cmake-utils/cmake)
include(eil_check_idf_features)
eil_check_idf_has_esp_drivers()

set(req esp_timer)

idf_component_register(
    INCLUDE_DIRS .
    SRCS lib8tion.c
    REQUIRES ${req}
)

include(eil_ci)
