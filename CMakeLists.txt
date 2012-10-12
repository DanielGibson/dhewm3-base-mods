# this CMakeLists.txt is  supposed to be used (with add_subdirectory())
# from CMakeLists.txt in neo/mods/ which in turn is supposed to be used
# (with add_subdirectory()...) from CMakeLists.txt in neo/

# Denton's Enhanced Doom3 (dentonmod) (based on base game)

# it's based on the base game (from game/), so use corresponding source files
# and add the dentonmod-specific files (tracer.cpp)
set(src_dentonmod
	${src_game_mods} # defined in neo/mods/CMakeLists.txt
	tracer.cpp
)

# SETUP_MOD( name srclist compile_defs ) - also from neo/mods/CMakeLists.txt
# make sure to have quotes around srclist!
SETUP_MOD("dentonmod" "${src_dentonmod}" "GAME_DLL;_PORTALSKY;_DENTONMOD")
