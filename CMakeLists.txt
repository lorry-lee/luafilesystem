
set(LUA_FILE_SYSTEM_SOURCES 
    src/lfs.c
)

file(GLOB LUA_FILE_SYSTEM_INCLUDE_FILES "src/*.h")

add_library(luafilesystem STATIC ${LUA_FILE_SYSTEM_SOURCES})

target_link_libraries(luafilesystem)

install_our_headers(${LUA_FILE_SYSTEM_INCLUDE_FILES})

set(LUA_FILE_SYSTEM_LINK_WITH luafilesystem PARENT_SCOPE)

#-----------------------------------------------------------------------------#
# vim: set ts=8 sts=4 sw=4 et:
