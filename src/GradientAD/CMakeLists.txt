
set(GradientAD_SOURCE GradientAD.cxx)
GENERATECLP(GradientAD_SOURCE GradientAD.cxx)


add_executable(GradientAD_${MYHAWKID} ${GradientAD_SOURCE})
target_link_libraries(GradientAD_${MYHAWKID} ${ITK_LIBRARIES})

SEMMacroBuildCLI(
        NAME GradientAD
        LOGO_HEADER ${Slicer_SOURCE_DIR}/Resources/NAMICLogo.h
        ADDITIONAL_SRCS
        GradientAD.cxx
        TARGET_LIBRARIES ModuleDescriptionParser ${ITK_LIBRARIES} vtkTeem MRMLCore SlicerBaseCLI ${VTK_LIBRARIES}
        INCLUDE_DIRECTORIES
        ${vtkTeem_INCLUDE_DIRS}
        ${MRMLCore_INCLUDE_DIRS}
        ${vtkITK_INCLUDE_DIRS}
        ${SlicerBaseCLI_SOURCE_DIR} ${SlicerBaseCLI_BINARY_DIR}
)