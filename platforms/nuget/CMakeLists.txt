# --------------------------------------------------------
#  Copyright (C) 2004-2017 by EMGU Corporation. All rights reserved.
# --------------------------------------------------------

IF (WIN32 AND (HAVE_WINDESKTOP_X86 OR HAVE_WINDESKTOP_X64) )

PROJECT(Emgu.TF.nuget)
ADD_CUSTOM_TARGET(
   ${PROJECT_NAME}
   COMMAND ${CMAKE_CURRENT_SOURCE_DIR}/../../miscellaneous/nuget.exe pack Package.nuspec

)
ADD_DEPENDENCIES(${PROJECT_NAME} Emgu.TF.World)

ENDIF()
