
set(DifferenceOfGaussians_SOURCE DifferenceOfGaussians.cxx)
GENERATECLP(DifferenceOfGaussians_SOURCE DifferenceOfGaussians.cxx)


add_executable(DifferenceOfGaussians_${MYHAWKID} ${DifferenceOfGaussians_SOURCE})
target_link_libraries(DifferenceOfGaussians_${MYHAWKID} ${ITK_LIBRARIES})
