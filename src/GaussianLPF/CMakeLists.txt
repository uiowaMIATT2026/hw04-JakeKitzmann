
set(GaussianLPF_SOURCE Gaussian.cxx)
GENERATECLP(GaussianLPF_SOURCE Gaussian.xml)


add_executable(GaussianLPF_${MYHAWKID} ${GaussianLPF_SOURCE})
target_link_libraries(GaussianLPF_${MYHAWKID} ${ITK_LIBRARIES})

