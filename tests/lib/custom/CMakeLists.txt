# Copyright (c) 2021, Legrand North America, LLC.
# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)
#find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
find_package(Zephyr COMPONENTS unittest REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(app_lib_custom_test)

target_include_directories(testbinary PRIVATE ../../../include/)
target_sources(testbinary PRIVATE src/main.c ../../../lib/custom/custom.c)
