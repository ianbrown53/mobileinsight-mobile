all: diag_revealer

# Default ndk build command. If ndk-build is not available, set the path manually.
ndk-build ?= ndk-build
# ndk-build=/vagrant/android-ndk-r28b-linux/android-ndk-r28b/toolchains/llvm/prebuilt/linux-x86_64/bin/aarch64-linux-android21-clang diag_revealer.c

diag_revealer:
	$(ndk-build)
	cp ../libs/arm64-v8a/diag_revealer .
	rm -r ../obj/ ../libs/
	cp ./diag_revealer ../../../app/data/
	echo "diag_revealer has been copied to ../../../app/data/"

clean:
	rm diag_revealer
