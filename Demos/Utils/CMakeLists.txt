add_library(Utils
		FileSystem.h
		Hashmap.h
		IndexedFaceMesh.cpp
		IndexedFaceMesh.h
		IndexedTetMesh.cpp
		IndexedTetMesh.h
		Logger.h
		ObjectArray.h
		OBJLoader.h
		SceneLoader.cpp
		SceneLoader.h
		StringTools.h
		TetGenLoader.cpp
		TetGenLoader.h
		Timing.h
		VolumeIntegration.cpp
		VolumeIntegration.h

		CMakeLists.txt
)

find_package( Eigen3 REQUIRED )
include_directories( ${EIGEN3_INCLUDE_DIR} )

install(TARGETS Utils
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib)

install(DIRECTORY .
DESTINATION include/Demos/Utils
FILES_MATCHING PATTERN "*.h")




