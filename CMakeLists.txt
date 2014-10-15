cmake_minimum_required (VERSION 2.8)

# ---------- LuaLib ----------
project ( LuaLib )

IF (${MSVC})
	ADD_DEFINITIONS(/D "_CRT_SECURE_NO_WARNINGS")
ENDIF(${MSVC})

SET( LUA_SRCS "${PROJECT_SOURCE_DIR}/src" )

SET ( INCLUDES
	"${LUA_SRCS}/lapi.h"
	"${LUA_SRCS}/lauxlib.h"
	"${LUA_SRCS}/lcode.h"
	"${LUA_SRCS}/lctype.h"
	"${LUA_SRCS}/ldebug.h"
	"${LUA_SRCS}/ldo.h"
	"${LUA_SRCS}/lfunc.h"
	"${LUA_SRCS}/lgc.h"
	"${LUA_SRCS}/llex.h"
	"${LUA_SRCS}/llimits.h"
	"${LUA_SRCS}/lmem.h"
	"${LUA_SRCS}/lobject.h"
	"${LUA_SRCS}/lopcodes.h"
	"${LUA_SRCS}/lparser.h"
	"${LUA_SRCS}/lstate.h"
	"${LUA_SRCS}/lstring.h"
	"${LUA_SRCS}/ltable.h"
	"${LUA_SRCS}/ltm.h"
	"${LUA_SRCS}/lua.h"
	"${LUA_SRCS}/luaconf.h"
	"${LUA_SRCS}/lualib.h"
	"${LUA_SRCS}/lundump.h"
	"${LUA_SRCS}/lvm.h"
	"${LUA_SRCS}/lzio.h"
)

SET ( SRCS
	"${LUA_SRCS}/lapi.c"
	"${LUA_SRCS}/lauxlib.c"
	"${LUA_SRCS}/lbaselib.c"
	"${LUA_SRCS}/lbitlib.c"
	"${LUA_SRCS}/lcode.c"
	"${LUA_SRCS}/lcorolib.c"
	"${LUA_SRCS}/lctype.c"
	"${LUA_SRCS}/ldblib.c"
	"${LUA_SRCS}/ldebug.c"
	"${LUA_SRCS}/ldo.c"
	"${LUA_SRCS}/ldump.c"
	"${LUA_SRCS}/lfunc.c"
	"${LUA_SRCS}/lgc.c"
	"${LUA_SRCS}/linit.c"
	"${LUA_SRCS}/liolib.c"
	"${LUA_SRCS}/llex.c"
	"${LUA_SRCS}/lmathlib.c"
	"${LUA_SRCS}/lmem.c"
	"${LUA_SRCS}/loadlib.c"
	"${LUA_SRCS}/lobject.c"
	"${LUA_SRCS}/lopcodes.c"
	"${LUA_SRCS}/loslib.c"
	"${LUA_SRCS}/lparser.c"
	"${LUA_SRCS}/lstate.c"
	"${LUA_SRCS}/lstring.c"
	"${LUA_SRCS}/lstrlib.c"
	"${LUA_SRCS}/ltable.c"
	"${LUA_SRCS}/ltablib.c"
	"${LUA_SRCS}/ltm.c"
	"${LUA_SRCS}/lua.c"
	"${LUA_SRCS}/luac.c"
	"${LUA_SRCS}/lundump.c"
	"${LUA_SRCS}/lvm.c"
	"${LUA_SRCS}/lzio.c"
)

add_library( lua STATIC
	${INCLUDES}
	${SRCS}
)
