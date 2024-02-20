# cppplayground
This is my CMake and C++ playground. The structure, CI/CD pipelins, deployment etc are tested here.

The goal is to have structure which I can use with ROS. 

Goals:
* Testability - unit testing, integration testing etc.
* CI/CD pipelines
  * Everything is not built when something changes
* Good library structure
* Deployment thinking
  * The environment is still unknown 
  * This is not actually in scope of this as this just outputs 2 different appications and share one or two libraries
* Building for different architectures x64/IA64 and ARM

## Building

To build all run: `cmake --build .` at the root directory of the project.
The outputs are created to the directory 
`build/<oprating system>/<processor architecture>`

To build single component the building is done with
`cmake --build . -t <target>`.

To see all targets:
`cmake --build . -t help`.

## Design decisisons

* There