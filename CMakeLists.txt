# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(workshop)

target_sources_ifdef(CONFIG_MAIN app PRIVATE src/main.c)
target_sources_ifdef(CONFIG_BLINK app PRIVATE src/blink.c)