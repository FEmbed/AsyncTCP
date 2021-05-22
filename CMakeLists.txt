idf_build_get_property(components_to_build BUILD_COMPONENTS)

set(srcs    "src/AsyncTCP.cpp")
set(include "src")

idf_component_register(SRCS "${srcs}"
                       INCLUDE_DIRS ${include}
                       REQUIRES "FEmbed-Arduino FEmbed-OS lwip"
                       PRIV_REQUIRES ${priv_requires})

target_compile_options(${COMPONENT_LIB} PRIVATE -fno-rtti)
