
set(CurvatureAD_SOURCE CurvatureAD.cxx)
GENERATECLP(CurvatureAD_SOURCE CurvatureAD.cxx)


add_executable(CurvatureAD_${MYHAWKID} ${CurvatureAD_SOURCE})
target_link_libraries(CurvatureAD_${MYHAWKID} ${ITK_LIBRARIES})

SEMMacroBuildCLI(
        NAME CurvatureAD
        LOGO_HEADER ${Slicer_SOURCE_DIR}/Resources/NAMICLogo.h
        ADDITIONAL_SRCS
        CurvatureAD.cxx
        TARGET_LIBRARIES ModuleDescriptionParser ${ITK_LIBRARIES} vtkTeem MRMLCore SlicerBaseCLI ${VTK_LIBRARIES}
        INCLUDE_DIRECTORIES
        ${vtkTeem_INCLUDE_DIRS}
        ${MRMLCore_INCLUDE_DIRS}
        ${vtkITK_INCLUDE_DIRS}
        ${SlicerBaseCLI_SOURCE_DIR} ${SlicerBaseCLI_BINARY_DIR}
)