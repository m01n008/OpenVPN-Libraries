# OpenVPN Libraries
- **Versions**: OpenVPN 2.6.9, OpenSSL 1.1.1w
- **Architectures**: ARM64, ARMv7, x86, x86_64
- **Artifacts**:
  - `android_libs/lib/*/libopenvpn.so`: JNI libraries
  - `android_libs/assets/pie_openvpn.*`: Executables
- **Integration**:
  1. Place libraries in `app/src/main/jniLibs/[arch]/`.
  2. Place executables in `app/src/main/assets/`.
  3. Update `libopenvpn.c` package name (e.g., `com.client.openvpn`).
  4. Call `startOpenVPN(configPath, binaryPath)` from Java/Kotlin.
- **Testing**: Verified 16KB alignment and ARM64 functionality.
