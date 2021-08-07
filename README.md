# Poco Parts
Add in **device.mk** or **common.mk**:
```makefile
$(call inherit-product-if-exists, vendor/PocoParts/pocoparts.mk)
```

### Dirac/MI Sound Enhancer

Add this to your **audio_effects.xml**
```xml
     <library name="dirac" path="libdirac.so"/>
     <effect name="dirac" library="dirac" uuid="e069d9e0-8329-11df-9168-0002a5d5c51b"/>
```
## Dependencies
Add this in your **$rom.dependencies**:

```
{
   "repository":   "dotOS-Devices/vendor_PocoParts",
   "target_path":  "vendor/PocoParts",
   "remote":       "github",
   "branch":       "dot11"
}
```
