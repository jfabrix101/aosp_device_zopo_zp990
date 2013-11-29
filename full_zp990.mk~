# Copyright (C) 2011 The Android Open Source Project
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# The gps config appropriate for this device
$(call inherit-product, device/common/gps/gps_eu.mk)

# full-languages (>= Android 4.2)
$(call inherit-product, $(SRC_TARGET_DIR)/product/full.mk)

# Inherit non-open-source blobs.
$(call inherit-product-if-exists, $(LOCAL_PATH)/vendor.mk)


# --- DEVICE_PACKAGE_OVERLAYS
# Allows us to specify a directory that will form the basis of an overlay 
# that will be applied onto the AOSP’s sources, thereby allowing us to substitute
# default package resources with device-specific resources. 
# You’ll find this useful if you’d like to set custom layouts or colors for
# Launcher2 or other apps, for instance. 
DEVICE_PACKAGE_OVERLAYS := $(LOCAL_PATH)/overlay

# --- PRODUCT_PACKAGES
# Allows us to specify packages we’d like to have this product include in addition
# to those specified in the products we’re already inheriting from.
# If you have custom apps, binaries, or libraries located within device/<BRAND>/<DEVICE_NAME>/,
# for instance, you’ll want to add them here so that they are included in the final
# images generated.
# Notice the use of the += sign. It allows us to append to the existing values
# in the variable instead of substituting its content.
PRODUCT_PACKAGES +=


# --- PRODUCT_COPY_FILES
# Allows us to list specific files we’d like to see copied to the target’s
# filesystem and the location where they need to be copied.
# Each source/destination pair is colon-separated, and pairs are space-separated
# among themselves. This is useful for configuration files and prebuilt binaries
# such as firmware images or kernel modules.
PRODUCT_COPY_FILES := \
    device/sample/etc/apns-full-conf.xml:system/etc/apns-conf.xml


#PRODUCT_COPY_FILES += \
#    $(LOCAL_PATH)/vold.fstab:system/etc/vold.fstab \
#    $(LOCAL_PATH)/init.vsnet:system/bin/init.vsnet \
#    $(LOCAL_PATH)/init.vsnet-down:system/bin/init.vsnet-down \
#    $(LOCAL_PATH)/gps_brcm_conf.xml:system/etc/gps_brcm_conf.xml

#PRODUCT_COPY_FILES += \
#    $(LOCAL_PATH)/prebuilt/wireless.ko:system/lib/modules/wireless.ko

# ----------

# --- PRODUCT_NAME
# The TARGET_PRODUCT, which you can set either by selecting a lunch combo or
# passing it as part of the combo parameter to lunch, as in: "lunch <PRODUCT_NAME>-eng"
PRODUCT_NAME := full_zp990

# --- PRODUCT_DEVICE
# The name of the actual finished product shipped to the customer. 
# TARGET_DEVICE derives from this variable. PRODUCT_DEVICE has to match an
# entry in device/<BRAND>/, since that’s where the build looks for the
# corresponding BoardConfig.mk. In this case, the variable is the same
# as the name of the directory we’re already in.
PRODUCT_DEVICE := zp990

# --- PRODUCT_BRAND
# Version 4.2/Jelly Bean also includes a PRODUCT_BRAND that is typically set to Android.
# The value of this variable is then available as the ro.product.brand global property.
# The latter is used by some parts of the stack that take action based on the device’s vendor.
PRODUCT_BRAND := Android

# The name of this product as provided in the “Model number” in the 
# “About the phone” section of the settings. This variable actually gets
# stored as the ro.product.model global property accessible on the device.
PRODUCT_MODEL := Full Android on ZP990


