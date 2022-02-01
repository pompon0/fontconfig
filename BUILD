package(
  default_visibility = ["//visibility:public"],
)

cc_library(
  name = "fontconfig",
  includes = ["."],
  hdrs = glob(["**/*.h"]),
  defines = [
    "HAVE_CONFIG_H",
    "FC_CACHEDIR='\"/var/cache/fontconfig\"'",
    "CONFIGDIR='\"/etc/fonts/conf.d\"'",
    "FONTCONFIG_PATH='\"/etc/fonts\"'",
    "FC_TEMPLATEDIR='\"/usr/share/fontconfig/conf.avail\"'",
  ],
  srcs = glob(["**/*.c"],exclude=["test/**","meson-cc-tests/**"]),
  deps = [
    "@org_freetype_freetype2//:freetype2",
    "@com_github_libexpat_libexpat//:expat",
  ],
)
