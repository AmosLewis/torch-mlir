add_mlir_conversion_library(TorchMLIRTorchOnnxToTorch
    ComMicrosoftDomain.cpp
    DefaultDomainAtoF.cpp
    DefaultDomainGtoP.cpp
    DefaultDomainQtoZ.cpp
    OnnxRecurrentLayerOpExpanders.cpp
    Passes.cpp
    Patterns.cpp
    TorchOnnxToTorch.cpp
    Utils.cpp

    ADDITIONAL_HEADER_DIRS
    ${PROJECT_SOURCE_DIR}/include/torch-mlir/Conversion/TorchOnnxToTorch

    DEPENDS
    TorchMLIRConversionTorchOnnxToTorchPassIncGen

    LINK_LIBS PUBLIC
    MLIRIR
    MLIRPass
    TorchMLIRTorchDialect
)
