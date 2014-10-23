cmake_minimum_required(VERSION 2.8)

set(MUSIC_QUALITY 3 CACHE STRING "Music quality [-1(very low) - 10(very high), fractional values allowed]")

if(NOT DEFINED COLOBOT_INSTALL_DATA_DIR)
    if(${CMAKE_SYSTEM_NAME} MATCHES "Windows")
        set(COLOBOT_INSTALL_MUSIC_DIR ${CMAKE_INSTALL_PREFIX}/data/music CACHE PATH "Colobot shared music directory")
    else()
        set(COLOBOT_INSTALL_MUSIC_DIR ${CMAKE_INSTALL_PREFIX}/share/games/colobot/music CACHE PATH "Colobot shared music directory")
    endif()
else()
    set(COLOBOT_INSTALL_MUSIC_DIR ${COLOBOT_INSTALL_DATA_DIR}/music CACHE PATH "Colobot shared music directory")
endif()

file(GLOB FLAC_FILES RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "*.flac")
foreach(FILE ${FLAC_FILES})
    message(STATUS "Converting ${FILE} to OGG...")
    get_filename_component(FILENAME ${FILE} NAME_WE)
    add_custom_command(
        OUTPUT ${FILENAME}.ogg
        COMMAND oggenc -q ${MUSIC_QUALITY} -o ${CMAKE_CURRENT_BINARY_DIR}/${FILENAME}.ogg ${CMAKE_CURRENT_SOURCE_DIR}/${FILE}
        DEPENDS ${FILE}
    )
    add_custom_target(convert-${FILE} ALL DEPENDS ${FILENAME}.ogg)
    install(FILES ${CMAKE_CURRENT_BINARY_DIR}/${FILENAME}.ogg DESTINATION ${COLOBOT_INSTALL_MUSIC_DIR})
endforeach()

file(GLOB OGG_FILES RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "*.ogg")
foreach(FILE ${OGG_FILES})
    message(STATUS "Installing ${FILE}...")
    install(FILES ${CMAKE_CURRENT_SOURCE_DIR}/${FILE} DESTINATION ${COLOBOT_INSTALL_MUSIC_DIR})
endforeach()

