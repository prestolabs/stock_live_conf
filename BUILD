# Copyright (c) 2021 Presto Labs Pte. Ltd.
# Author: sungraecho

package(default_visibility = ["//visibility:public"])

config_setting(name = "region_cn", define_values = {"region": "cn"})
config_setting(name = "region_hkex", define_values = {"region": "hkex"})
config_setting(name = "region_krx", define_values = {"region": "krx"})
config_setting(name = "region_tse", define_values = {"region": "tse"})
config_setting(name = "region_tw", define_values = {"region": "tw"})
config_setting(name = "region_us", define_values = {"region": "us"})

filegroup(
    name = "basic_data_config_files",
    data = glob(["basic_data/*/*",
                 "basic_data/*/*/*"]),
)

filegroup(
    name = "config_files",
    data = select({
        ":region_cn": [":config_files_cn"],
        ":region_hkex": [":config_files_hkex"],
        ":region_krx": [":config_files_krx"],
        ":region_tse": [":config_files_tse"],
        ":region_tw": [":config_files_tw"],
        ":region_us": [":config_files_us"],
        "//conditions:default": [":config_files_default"],
    }),
)

filegroup(
    name = "config_files_cn",
    data = glob(["cn/**/*"]),
)

filegroup(
    name = "config_files_hkex",
    data = glob(["hkex/**/*"]),
)

filegroup(
    name = "config_files_krx",
    data = glob(["krx/**/*"]),
)

filegroup(
    name = "config_files_tse",
    data = glob(["tse/**/*"]),
)

filegroup(
    name = "config_files_tw",
    data = glob(["tw/**/*"]),
)

filegroup(
    name = "config_files_us",
    data = glob(["us/**/*"]),
)

filegroup(
    name = "config_files_default",
    data = glob(["**/*"]),
)

filegroup(
    name = "external_info_files",
    data = glob(["**/external_info_keys.json"]),
)
