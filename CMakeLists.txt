cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

project(ULua VERSION 0.0.1)
message(STATUS "[Project] ${PROJECT_NAME}")

include(cmake/InitUCMake.cmake)
Ubpa_InitUCMake()

Ubpa_InitProject()

Ubpa_DownloadZip(
  https://ubpa.github.io/UData/ULua/lua/lua_5_3_2.zip
  lua_5_3_2.zip
  SHA256 9FD39FD3075C9ECF2A41F64B1F4440DDAEF7586E7F620F1625FD4016DD40ED57
)

include ( cmake/dist.cmake )
Ubpa_AddSubDirsRec(src)

Ubpa_Export(DIRECTORIES "include")
