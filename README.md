# AOSPA asteroids local manifest

Pinned source manifest for building Paranoid Android `calcite` for Nothing Phone (3a/3a Pro), codename `asteroids`.

## Use

Initialize the standard AOSPA tree, then clone this repository into `.repo/local_manifests`:

```bash
repo init -u https://github.com/AOSPA/manifest -b calcite
rm -rf .repo/local_manifests
git clone -b calcite https://github.com/fruity-aospa/local_manifest .repo/local_manifests
repo sync --current-branch --no-tags -j4
```

Build with AOSPA's official helper:

```bash
./vendor/aospa/build.sh asteroids
```

`asteroids.xml` pins all asteroids-specific and successful-build override projects to immutable commits in `fruity-aospa`. Private signing keys and generated build artifacts are not included.
