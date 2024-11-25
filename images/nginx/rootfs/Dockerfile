# Copyright 2024 The Kubernetes Authors. All rights reserved.
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

# Start from Alpine 3.20.3.
FROM alpine:3.20.3

# Install dependencies.
RUN apk add \
    libc-dev \
    make \
    gcc

# Change working directory.
WORKDIR /build/luajit2

# Download LuaJIT.
ADD https://github.com/openresty/luajit2/archive/v2.1-20241113.tar.gz luajit2.tar.gz

# Extract LuaJIT.
RUN tar --extract --file luajit2.tar.gz --strip-components 1

# Install LuaJIT.
RUN make install
