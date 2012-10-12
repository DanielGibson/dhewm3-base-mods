# this CMakeLists.txt is  supposed to be used (with add_subdirectory())
# from CMakeLists.txt in neo/mods/ which in turn is supposed to be used
# (with add_subdirectory()...) from CMakeLists.txt in neo/

# base game (as an example and to branch mods from)

# it's based on the base game (from game/), so use corresponding source files
# and add the dentonmod-specific files (tracer.cpp)
set(src_basegame
	${src_game_mods} # defined in neo/mods/CMakeLists.txt
	# add mod specific source (*.cpp) file here
	# and here etc (one per line)
)

# SETUP_MOD( name srclist compile_defs ) - also from neo/mods/CMakeLists.txt
# make sure to have quotes around srclist!
SETUP_MOD("base" "${src_basegame}" "GAME_DLL")
