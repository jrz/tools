# Various tools
- [Swift Script Caching Compiler](#-swift-script-caching-compiler)

## Swift Script Caching Compiler

This utility automatically manages Swift script execution by intelligently switching between interpretation and compilation modes. It is indented as a drop-in replacement for the Swift shebang in Swift scripts (```#!/usr/bin/env swift-scc``` intead of ```#!/usr/bin/env swift```)

### INSTALLATION:
Copy the script somewhere in your path

### USAGE:
Replace your ```#!/usr/bin/env swift``` with ```#!/usr/bin/env swift-scc```

### BENEFITS:
- Eliminates Swift's interpreter startup overhead for faster performance
- Caches compiled binaries to avoid unnecessary recompilation
- Optimizes for development speed during initial iterations
- Ensures maximum performance in automated/non-interactive contexts

### BEHAVIOR:
- In non-interactive mode: immediately compiles if needed and executes the binary
- In interactive terminal: uses interpreter for first 3 executions, then compiles
- Maintains a cached binary that's automatically rebuilt when the source script changes
