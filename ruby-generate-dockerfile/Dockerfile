# Copyright 2017 Google Inc.
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

# Use the Ruby base image to get Ruby and its dependencies.
FROM ruby-base

ARG BASE_IMAGE=ruby-base
ARG BUILD_TOOLS_IMAGE=ruby-build-tools

# Install the Dockerfile generation script and template.
COPY app/ /app/

ENV RUBY_BASE_IMAGE=$BASE_IMAGE \
    RUBY_BUILD_TOOLS_IMAGE=$BUILD_TOOLS_IMAGE

# The entry point runs the generation script.
ENTRYPOINT ["/app/generate_dockerfile.sh"]
