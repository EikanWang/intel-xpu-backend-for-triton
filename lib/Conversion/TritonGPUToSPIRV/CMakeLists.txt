add_mlir_conversion_library(TritonGPUToSPIRV
    TritonGPUToSPIRV.cpp
    ViewOpToSPIRV.cpp
    ElementwiseOpToSPIRV.cpp
    TritonGPUToSPIRVPass.cpp
    ConvertLayoutOpToSPIRV/SharedToDotOperandFMA.cpp
    ConvertLayoutOpToSPIRV.cpp
    DotOpToSPIRV/FMA.cpp
    LoadStoreOpToSPIRV.cpp
    ReduceOpToSPIRV.cpp
    TypeConverter.cpp
    Utility.cpp
    DotOpToSPIRV.cpp


    ADDITIONAL_HEADER_DIRS
    ${PROJECT_SOURCE_DIR}/include/triton/Conversion/TritonGPUToSPIRV

    DEPENDS
    TritonGPUToSPIRVConversionPassIncGen

    LINK_COMPONENTS
    Core

    LINK_LIBS PUBLIC
    MLIRIR
    MLIRPass
    MLIRGPUOps
    MLIRGPUTransforms
    TritonAnalysis
    TritonIR
    TritonGPUIR
    TritonGPUTransforms
)
