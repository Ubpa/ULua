Ubpa_AddTarget(
  MODE EXE
  RET_TARGET_NAME lua
  LIB
    Ubpa::ULua_core
  SOURCE
    "lua.rc"
  INC_PRIVATE
    "${PROJECT_SOURCE_DIR}/src/common"
    "${PROJECT_SOURCE_DIR}/include/ULua"
)

set_target_properties ( ${luac} PROPERTIES OUTPUT_NAME lua CLEAN_DIRECT_OUTPUT 1 )
