
set(Gaussian_SOURCE Gaussian.cxx)
GENERATECLP(Gaussian_SOURCE Gaussian.xml)


add_executable(Gaussian_${MYHAWKID} ${Gaussian_SOURCE})
target_link_libraries(Gaussian_${MYHAWKID} ${ITK_LIBRARIES})

SEMMacroBuildCLI(
        NAME Gaussian
        LOGO_HEADER ${Slicer_SOURCE_DIR}/Resources/NAMICLogo.h
        ADDITIONAL_SRCS
        Gaussian.cxx
        TARGET_LIBRARIES ModuleDescriptionParser ${ITK_LIBRARIES} vtkTeem MRMLCore SlicerBaseCLI ${VTK_LIBRARIES}
        INCLUDE_DIRECTORIES
        ${vtkTeem_INCLUDE_DIRS}
        ${MRMLCore_INCLUDE_DIRS}
        ${vtkITK_INCLUDE_DIRS}
        ${SlicerBaseCLI_SOURCE_DIR} ${SlicerBaseCLI_BINARY_DIR}
)