#
# Copyright (c) 2018 Nordic Semiconductor
#
# SPDX-License-Identifier: LicenseRef-BSD-5-Clause-Nordic
#
zephyr_library()
zephyr_library_link_libraries(nrf_bluetooth)

zephyr_library_sources_ifdef(CONFIG_NRF_BT_SVC_COMMON svc_common.c)
zephyr_library_sources_ifdef(CONFIG_BT_GATT_DM gatt_dm.c)
zephyr_library_sources_ifdef(CONFIG_BT_SCAN scan.c)