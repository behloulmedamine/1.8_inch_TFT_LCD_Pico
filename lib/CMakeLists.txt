add_library(Lib STATIC
    src/fonts.c
    src/st7735.c
)

#add target libraries
target_link_libraries(Lib pico_stdlib hardware_gpio hardware_spi)
target_include_directories(Lib PUBLIC inc/)