Ubpa_AddTarget(
  MODE EXE
  OUTPUT_NAME lua
  LIB
    Ubpa::ULua_core
  SOURCE
    "lua.rc"
  INC_PRIVATE
    "${PROJECT_SOURCE_DIR}/src/common"
    "${PROJECT_SOURCE_DIR}/include/ULua"
)
