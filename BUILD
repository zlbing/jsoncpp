package(default_visibility = ["//visibility:public"])

COPTS = ["-std=c++11"]

LINK_OPTS = []

cc_library(
  name="jsoncpp",
  srcs = glob([
      "jsoncpp_dist/**/*.cpp"
      ]),
  hdrs = glob([
      "jsoncpp_dist/**/*.h"
      ]),
  includes = ["jsoncpp_dist"],
  copts = COPTS,
  linkopts = LINK_OPTS,
  linkstatic = True,
  deps = [
  ]
)
