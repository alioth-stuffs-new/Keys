# lunaris-priv_keys-template

# Usage

```bash
croot && git clone https://github.com/Lunaris-AOSP/vendor_lunaris-priv_keys vendor/lunaris-priv/keys
```

```bash
cd vendor/lunaris-priv/keys
```

```
./keys.sh
```

# Testing

Included `check_keys.py` script checks whether all apk/apex/capex files in the build out are signed with keys within its directory. Be aware that some targets are **expected** to be signed with vendor key, for example `com.android.apex.cts.shim.v1_prebuilt`.

```
$ ./check_keys.py ~/lunaris/out/target/product/Pong
/home/ab/lunaris/out/target/product/Pong/obj/ETC/com.android.apex.cts.shim.v1_prebuilt_intermediates/com.android.apex.cts.shim.apex is signed with an unknown key!
```
