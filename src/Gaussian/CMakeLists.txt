
set(Gaussian_SOURCE Gaussian.cxx)
GENERATECLP(Gaussian_SOURCE Gaussian.xml)


add_executable(Gaussian_${MYHAWKID} ${Gaussian_SOURCE})
target_link_libraries(Gaussian_${MYHAWKID} ${ITK_LIBRARIES})

