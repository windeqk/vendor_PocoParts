# Poco Parts
Add in **device.mk** or **common.mk**:  [*Example commit*](https://github.com/windeqk/device_xiaomi_surya/commit/a0709d7a2ae3ea8388636a517dce2d0e4efa3ef9#diff-247ee86229a709a6e2eedfc1d3c4a557825aee073e20b0112ab76f4ca8e4bc4e)
```makefile
$(call inherit-product-if-exists, vendor/PocoParts/pocoparts.mk)
```
Add to the top of the **init.qcom.rc** or other **init.rc**:     [*Example commit*](https://github.com/windeqk/device_xiaomi_surya/commit/c7be5b48b1bb4050575ac13992a4b7692eee3031)
```rc
import /vendor/etc/init/hw/init.pocoparts.rc
```



### Dirac/MI Sound Enhancer

Add this to your **audio_effects.xml**
```xml
     <library name="dirac" path="libdirac.so"/>
     <effect name="dirac" library="dirac" uuid="e069d9e0-8329-11df-9168-0002a5d5c51b"/>
```
## Dependencies
Add this in your **$rom.dependencies**:      [*Example commit*](https://github.com/windeqk/device_xiaomi_surya/commit/a0709d7a2ae3ea8388636a517dce2d0e4efa3ef9#diff-7e765a5169613eb0cc5d4ed1bb9c52cca0c6bfa5ce1175623ba9b9475d3fe47e)

```
{
   "repository":   "dotOS-Devices/vendor_PocoParts",
   "target_path":  "vendor/PocoParts",
   "remote":       "github",
   "branch":       "dot11"
}
```
