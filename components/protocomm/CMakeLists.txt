set(COMPONENT_ADD_INCLUDEDIRS include/common
                              include/security
                              include/transports)
set(COMPONENT_PRIV_INCLUDEDIRS proto-c src/common)
set(COMPONENT_SRCS  "src/common/protocomm.c"
                    "src/security/security0.c"
                    "src/security/security1.c"
                    "proto-c/constants.pb-c.c"
                    "proto-c/sec0.pb-c.c"
                    "proto-c/sec1.pb-c.c"
                    "proto-c/session.pb-c.c"
                    "src/transports/protocomm_httpd.c")

set(COMPONENT_PRIV_REQUIRES protobuf-c mbedtls wifi_provisioning)

register_component()
