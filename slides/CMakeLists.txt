cmake_minimum_required(VERSION 3.17)

project(HPCBPCodeReviewOctober12)

find_program(PANDOC pandoc)

add_custom_target(slides ALL
    COMMAND
    ${PANDOC} -s slides.md -o ${CMAKE_BINARY_DIR}/slides.html
    -t revealjs
    -V revealjs-url=https://unpkg.com/reveal.js@^4
    -V theme=white
    -V transition=none
    -V backgroundTransition=none
    -V slideNumber=true
    --include-in-header=slides.css
    --highlight-style zenburn
    WORKING_DIRECTORY ${CMAKE_SOURCE_DIR}
    DEPENDS ${CMAKE_SOURCE_DIR}/slides.md
    )

set(CMAKE_INSTALL_PREFIX ${CMAKE_BINARY_DIR})
install(FILES ${CMAKE_BINARY_DIR}/slides.html DESTINATION generated)
install(DIRECTORY img DESTINATION generated)
