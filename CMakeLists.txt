cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

project(ULua VERSION 0.1.1)
message(STATUS "[Project] ${PROJECT_NAME}")

include(cmake/InitUCMake.cmake)
Ubpa_InitUCMake()

Ubpa_InitProject()

Ubpa_DownloadZip(
  https://cdn.jsdelivr.net/gh/Ubpa/UData@master/ULua/lua/lua_5_3_2.zip
  lua_5_3_2.zip
  SHA256 9FD39FD3075C9ECF2A41F64B1F4440DDAEF7586E7F620F1625FD4016DD40ED57
)

include ( cmake/dist.cmake )
Ubpa_AddSubDirsRec(src)

Ubpa_Export(
  TARGET
  DIRECTORIES
    "include"
)
