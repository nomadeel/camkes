#
# Copyright 2018, Data61
# Commonwealth Scientific and Industrial Research Organisation (CSIRO)
# ABN 41 687 119 230.
#
# This software may be distributed and modified according to the terms of
# the BSD 2-Clause license. Note that NO WARRANTY is provided.
# See "LICENSE_BSD2.txt" for details.
#
# @TAG(DATA61_BSD)
#

cmake_minimum_required(VERSION 3.7.2)

add_subdirectory(components/Printer)
add_subdirectory(components/Server)

add_subdirectory(interfaces/GetterIface)
add_subdirectory(interfaces/PrinterIface)

# Now add our search directories so that the the components and interfaces are
# actually found by camkes
CAmkESAddImportPath(components interfaces)
