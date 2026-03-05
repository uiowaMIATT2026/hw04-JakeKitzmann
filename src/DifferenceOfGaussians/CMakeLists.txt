
set(DifferenceOfGaussians_SOURCE DifferenceOfGaussians.cxx)
GENERATECLP(DifferenceOfGaussians_SOURCE DifferenceOfGaussians.cxx)


add_executable(DifferenceOfGaussians_${MYHAWKID} ${DifferenceOfGaussians_SOURCE})
target_link_libraries(DifferenceOfGaussians_${MYHAWKID} ${ITK_LIBRARIES})

SEMMacroBuildCLI(
        NAME DifferenceOfGaussians
        LOGO_HEADER ${Slicer_SOURCE_DIR}/Resources/NAMICLogo.h
        ADDITIONAL_SRCS
        DifferenceOfGaussians.cxx
        TARGET_LIBRARIES ModuleDescriptionParser ${ITK_LIBRARIES} vtkTeem MRMLCore SlicerBaseCLI ${VTK_LIBRARIES}
        INCLUDE_DIRECTORIES
        ${vtkTeem_INCLUDE_DIRS}
        ${MRMLCore_INCLUDE_DIRS}
        ${vtkITK_INCLUDE_DIRS}
        ${SlicerBaseCLI_SOURCE_DIR} ${SlicerBaseCLI_BINARY_DIR}
)