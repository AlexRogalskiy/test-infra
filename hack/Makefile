# Copyright 2022 The Kubernetes Authors.
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

include ../Makefile.base.mk
# Makefile.base.mk requires REPO_ROOT to be set
REPO_ROOT:=${CURDIR}/..

# ARGS can be overridden by calling make
ARGS ?= ""

run-coalesce: ensure-py-requirements3
	../hack/run-in-python-container.sh ./hack/coalesce.py ${ARGS}
.PHONY: run-compare-yaml

test-coalesce: ensure-py-requirements3
	../hack/run-in-python-container.sh ./hack/coalesce_test.py
.PHONY: test-coalesce
