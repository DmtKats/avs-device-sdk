add_definitions("-DACSDK_LOG_MODULE=equalizer")

add_library(EqualizerImplementations SHARED
        EqualizerController.cpp
        EqualizerUtils.cpp
        EqualizerLinearBandMapper.cpp
        InMemoryEqualizerConfiguration.cpp
        MiscDBEqualizerStorage.cpp
        SDKConfigEqualizerConfiguration.cpp
    )

set_target_properties(EqualizerImplementations PROPERTIES VERSION ${PROJECT_VERSION} SOVERSION ${PROJECT_VERSION_MAJOR} )

target_include_directories(EqualizerImplementations PUBLIC
    "${EqualizerImplementations_SOURCE_DIR}/include"
    )

target_link_libraries(EqualizerImplementations AVSCommon)

# install target
asdk_install()
