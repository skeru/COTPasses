macro(add_cot_pass name)
  add_library(${name} OBJECT ${ARGN})
  set_property(TARGET ${name} PROPERTY POSITION_INDEPENDENT_CODE 1)
  llvm_update_compile_flags(${name})
endmacro()


add_subdirectory(FunctionEraser)
add_subdirectory(HelloLLVM)
add_subdirectory(InstructionCount)
