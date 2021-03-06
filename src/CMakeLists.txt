#
# src/CMakeLists.txt
# HRVO Library
#
# Copyright 2009 University of North Carolina at Chapel Hill
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
# Please send all bug reports to <geom@cs.unc.edu>.
#
# The authors may be contacted via:
#
# Jamie Snape, Jur van den Berg, Stephen J. Guy, and Dinesh Manocha
# Dept. of Computer Science
# 201 S. Columbia St.
# Frederick P. Brooks, Jr. Computer Science Bldg.
# Chapel Hill, N.C. 27599-3175
# United States of America
#
# <http://gamma.cs.unc.edu/HRVO/>
#

set(HRVO_HEADERS
	API.h
	HRVO.h
	Simulator.h
	Vector2.h)

set(HRVO_SOURCES
	Agent.cpp
	Agent.h
	Definitions.h
	Goal.cpp
	Goal.h
	KdTree.cpp
	KdTree.h
	Simulator.cpp
	Vector2.cpp)

add_library(HRVO ${HRVO_HEADERS} ${HRVO_SOURCES})

install(FILES ${HRVO_HEADERS} DESTINATION include)
install(TARGETS HRVO DESTINATION lib)
