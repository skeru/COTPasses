add_library(COTPasses MODULE
 ForceLinking.cpp
 $<TARGET_OBJECTS:FunctionEraser>
 $<TARGET_OBJECTS:HelloLLVM>
 $<TARGET_OBJECTS:InstructionCount>
)

set_target_properties(COTPasses PROPERTIES PREFIX "" SUFFIX "${LLVM_PLUGIN_EXT}")
