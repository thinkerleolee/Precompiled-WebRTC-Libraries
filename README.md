# Precompiled-WebRTC-Libraries
* buildtools by https://github.com/vsimon/webrtcbuilds

# Package Contents
```
webrtcbuilds-<rev>-<sha>-<target-os>-<target-cpu>
|
├── bin
│   └── <webrtc programs>
├── include
│   └── <webrtc include files>
└── lib
    ├── Debug
    │   └── <webrtc library files>
    └── Release
    │   └── <webrtc library files>
    ├── ... 
```

# Usage

See [[how to build the peerconnection example|Building-the-peerconnection-example]].

Otherwise to compile a simple application, run the following command(s):

### Linux ###

    export PKG_CONFIG_PATH=$WEBRTCBUILDS_FOLDER/lib/Release/pkgconfig
    g++ -o test test.cpp \
      $(pkg-config --cflags --libs --define-variable=prefix=$WEBRTCBUILDS_FOLDER libwebrtc_full)
