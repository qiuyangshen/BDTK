# Copyright (c) 2022 Intel Corporation.
#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.

add_executable(NextgenCompilerTest NextgenCompilerTest.cpp)
target_link_libraries(NextgenCompilerTest ${EXECUTE_TEST_LIBS} nextgen)
add_test(NextgenCompilerTest ${EXECUTABLE_OUTPUT_PATH}/NextgenCompilerTest
         ${TEST_ARGS})

add_executable(ParserTest ParserTest.cpp)
target_link_libraries(ParserTest ${EXECUTE_TEST_LIBS} nextgen test_utils
                      cider_plan_parser)
add_test(ParserTest ${EXECUTABLE_OUTPUT_PATH}/ParserTest ${TEST_ARGS})
