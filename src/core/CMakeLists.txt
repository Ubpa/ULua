if ( LUA_BUILD_AS_DLL )
  set ( mode SHARED )
  set ( def "LUA_BUILD_AS_DLL" )
else()
  set ( mode STATIC )
  set ( def "" )
endif ()

Ubpa_AddTarget(
  MODE ${mode}
  RET_TARGET_NAME liblua
  INC
    "${PROJECT_SOURCE_DIR}/include"
  DEFINE_PRIVATE
    ${def}
  LIB_PRIVATE
    Ubpa::ULua_common
)

set_target_properties ( ${liblua} PROPERTIES OUTPUT_NAME lua CLEAN_DIRECT_OUTPUT 1 )
