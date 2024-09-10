## Directory structure
The directory structure is based on the
[pitchfork layout](https://github.com/vector-of-bool/pitchfork), and I describe it
more in [this video](https://www.youtube.com/watch?v=6oJ2LLxfP3s).

| Directory    | Description                                                  |
|--------------|--------------------------------------------------------------|
| build/       | Build output (object files + executable)                     |
| docs/        | Documentation (e.g., coding guidelines, images)              |
| src/         | Source files (.c/.h)                                         |
| src/app/     | Source files for the application layer (see SW architecture) |
| src/common/  | Source files for code used across the project                |
| src/drivers/ | Source files for the driver layer (see SW architecture)      |
| src/test/    | Source files related to test code                            |
| external/    | External dependencies (as git submodules if possible)        |
| tools/       | Scripts, configs, binaries                                   |
| .github/     | Configuration file for GitHub actions                        |

## Build
The two most common ways to build code for a microcontroller are from
an IDE (often supplied by the vendor) or from the command-line through a build
system (for example, make). There are pros and cons to both ways, and I describe
them in [this video](https://www.youtube.com/watch?v=H1HToCzku9Y) and
[this video](https://www.youtube.com/watch?v=HCfq44NNBaU).

In short, using an IDE is the most straightforward approach, but
at the same time less flexible because it forces you into a particular environment.
A build system is more complicated to set up, but it can be combined with your editor
of choice, gives more control over the build process, is great for automation (see CI),
and allows for a command-line based environment, which transfers better across projects.
This project can be built both ways, however, _make_ is the preferred way, but the IDE
is helpful when step-debugging the code.
