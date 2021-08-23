set(c_options_private "")
if(MSVC)
  list(APPEND c_options_private "/MP")
elseif("${CMAKE_CXX_COMPILER_ID}" STREQUAL "Clang")
  #
elseif("${CMAKE_CXX_COMPILER_ID}" STREQUAL "GNU")
  #
endif()

Ubpa_AddTarget(
  MODE EXE
  RET_TARGET_NAME luac
  SOURCE
    "luac.rc"
  LIB
    Ubpa::ULua_common
  INC
    "${PROJECT_SOURCE_DIR}/include"
  C_OPTION_PRIVATE
    ${c_options_private}
)

set_target_properties ( ${luac} PROPERTIES OUTPUT_NAME luac CLEAN_DIRECT_OUTPUT 1 )
