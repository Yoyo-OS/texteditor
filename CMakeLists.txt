cmake_minimum_required(VERSION 3.14)

project(yoyo-texteditor LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt5 COMPONENTS Core Widgets Quick REQUIRED)
find_package(KF5SyntaxHighlighting)

set(PROJECT_SOURCES
        src/main.cpp
        src/documenthandler.cpp
        src/highlightmodel.cpp
        src/texteditor.cpp
        qml.qrc
)

add_executable(yoyo-texteditor
  ${PROJECT_SOURCES}
)

target_link_libraries(yoyo-texteditor
  PRIVATE
  Qt5::Core
  Qt5::Widgets
  Qt5::Quick
  KF5::SyntaxHighlighting
  )

install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION /usr/bin)

install(FILES
      yoyo-texteditor.desktop
      DESTINATION /usr/share/applications/
      COMPONENT Runtime
)