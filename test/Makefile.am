#
# Copyright 2020 Comcast Cable Communications Management, LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
# SPDX-License-Identifier: Apache-2.0
#
AM_CFLAGS = -D_ANSC_LINUX
AM_CFLAGS += -D_ANSC_USER

AM_CPPFLAGS = -Wall -g -Werror
AM_CXXFLAGS = -std=c++11

ACLOCAL_AMFLAGS = -I m4
bin_PROGRAMS = libnet_gtest.bin
libnet_gtest_bin_CPPFLAGS = -I$(PKG_CONFIG_SYSROOT_DIR)$(includedir)/gtest \
                                        -I${top_srcdir}/gtest/include \
                                        -I${top_srcdir}/source \
                                        -I${top_srcdir}/source/include \
                                        -I$(PKG_CONFIG_SYSROOT_DIR)$(includedir)/dbus-1.0 \
                                        -I$(PKG_CONFIG_SYSROOT_DIR)$(libdir)/dbus-1.0/include \
                                        -I$(PKG_CONFIG_SYSROOT_DIR)$(includedir)/ccsp

libnet_gtest_bin_SOURCES = libnet_test.cpp gtest_main.cpp TestEnvironment.hpp TestUtils.cpp TestUtils.hpp
libnet_gtest_bin_LDFLAGS = -lgtest -lgmock -lgcov -pthread
libnet_gtest_bin_LDADD = ${top_builddir}/source/libnet.la
