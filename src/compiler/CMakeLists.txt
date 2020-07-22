Ubpa_AddTarget(
  MODE EXE
  RET_TARGET_NAME luac
  SOURCE
    "luac.rc"
  LIB
    Ubpa::ULua_common
  INC
    "${PROJECT_SOURCE_DIR}/include"
)

set_target_properties ( ${luac} PROPERTIES OUTPUT_NAME luac CLEAN_DIRECT_OUTPUT 1 )
