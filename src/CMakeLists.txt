cmake_minimum_required (VERSION 2.6)
project (lua)

set(SRC
lapi.c
lauxlib.c
lbaselib.c
lbitlib.c
lcode.c
lcorolib.c
lctype.c
ldblib.c
ldebug.c
ldo.c
ldump.c
lfunc.c
lgc.c
linit.c
liolib.c
llex.c
lmathlib.c
lmem.c
loadlib.c
lobject.c
lopcodes.c
loslib.c
lparser.c
lstate.c
lstring.c
lstrlib.c
ltable.c
ltablib.c
ltm.c
lua.c
lundump.c
lvm.c
lzio.c
)

add_executable(lua ${SRC})

add_library(lib SHARED ${SRC})
set_target_properties(lib PROPERTIES OUTPUT_NAME lua)