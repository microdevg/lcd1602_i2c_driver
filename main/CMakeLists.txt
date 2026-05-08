# 1. Buscamos todos los archivos .c en 'main' y sus subcarpetas
file(GLOB_RECURSE SOURCES "*.c")

# 2. Registramos el componente
idf_component_register(
    SRCS ${SOURCES}
    INCLUDE_DIRS "." "include"
    REQUIRES "driver"
)