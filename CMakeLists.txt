include(FindPythonInterp)
if(NOT PYTHONINTERP_FOUND)
  message(FATAL_ERROR
  "Unable to find Python interpreter, required for builds and testing.
  Please install Python or specify the PYTHON_EXECUTABLE CMake variable.")
endif()

if( ${PYTHON_VERSION_STRING} VERSION_LESS 2.7 )
  message(FATAL_ERROR "Python 2.7 or newer is required")
endif()

message(FATAL_ERROR "Python OKAY!" ${PYTHON_VERSION_STRING})
