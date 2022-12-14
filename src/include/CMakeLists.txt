install(FILES
  libcephsqlite.h
  DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

install(FILES
  rados/librados.h
  rados/rados_types.h
  rados/rados_types.hpp
  rados/librados_fwd.hpp
  rados/librados.hpp
  buffer.h
  buffer_fwd.h
  inline_memory.h
  page.h
  crc32c.h
  rados/objclass.h
  DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/rados)
if(WITH_LIBRADOSSTRIPER)
  install(FILES
    radosstriper/libradosstriper.h
    radosstriper/libradosstriper.hpp
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/radosstriper)
endif()

if(WITH_RBD)
  install(FILES
    rbd/features.h
    rbd/librbd.h
    rbd/librbd.hpp
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/rbd)
endif()

if(WITH_RADOSGW)
  install(FILES
    rados/librgw.h
    rados/rgw_file.h
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/rados)
endif()

if(WITH_LIBCEPHFS)
  install(FILES
    cephfs/libcephfs.h
    cephfs/ceph_ll_client.h
    cephfs/types.h
    DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/cephfs)
endif()
