# Copyright (C) 2022 The Qt Company Ltd.
# SPDX-License-Identifier: BSD-3-Clause

if(NOT QT_BUILD_STANDALONE_TESTS AND NOT QT_BUILDING_QT)
    cmake_minimum_required(VERSION 3.16)
    project(tst_manual_sensor_explorer_widgets LANGUAGES CXX)
    find_package(Qt6BuildInternals REQUIRED COMPONENTS STANDALONE_TEST)
endif()

#####################################################################
## sensor_explorer Binary:
#####################################################################

qt_internal_add_manual_test(tst_manual_sensor_explorer_widgets
    GUI
    SOURCES
        explorer.cpp explorer.h explorer.ui
        main.cpp
    LIBRARIES
        Qt::Sensors
        Qt::Widgets
    ENABLE_AUTOGEN_TOOLS
        uic
)
