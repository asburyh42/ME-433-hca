add_executable(project
  waves.c
  )

# pull in common dependencies
target_link_libraries(project pico_stdlib hardware_spi pico_binary_info)

pico_enable_stdio_usb(project 1) 
pico_enable_stdio_uart(project 0)

# create map/bin/hex file etc.
pico_add_extra_outputs(project)