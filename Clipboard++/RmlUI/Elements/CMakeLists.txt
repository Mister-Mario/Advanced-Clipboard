add_library(Elements STATIC
    ElementClipboard.h
    ElementClipboard.cpp
    ElementFileManager.h
    ElementFileManager.cpp
    ElementShortcuts.h
    ElementShortcuts.cpp
    ElementEdit.h
    ElementEdit.cpp
)

# Set include directories
target_include_directories(Elements 
    PUBLIC 
        ${CMAKE_CURRENT_SOURCE_DIR}  # For local includes
    PRIVATE
        ${CMAKE_SOURCE_DIR}  # To allow includes relative to project root
)

# Link dependencies
target_link_libraries(Elements 
    PUBLIC 
        RmlUi::RmlUi
    PRIVATE 
        QClipboard
        ProjectUtils
        ViewModels
        EventHandlers
)