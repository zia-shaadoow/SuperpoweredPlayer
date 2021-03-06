# SuperpoweredPlayer - "the missing demo"
Real-time time stretching and pitch-shifting of audio files with Superpowered SDK in this simple demo for Android

![alt text](https://raw.githubusercontent.com/peteee/SuperpoweredPlayer/2224e0fa48f90474184ebbcfd94ad4be700ac546/spplayer_demo_screenshot.jpeg)

This extends the PlayerExample with the following:
```c++
// onSpeedSlider - Handle TimeStretching events.
extern "C" JNIEXPORT void
Java_com_superpowered_playerexample_MainActivity_onSpeedSlider (
        JNIEnv * __unused env,
        jobject __unused obj,
        jint value
) {
    player->setTempo((value/10000.0), true);
}

// onPitchSlider - Handle PitchShifting events.
extern "C" JNIEXPORT void
Java_com_superpowered_playerexample_MainActivity_onPitchSlider (
        JNIEnv * __unused env,
        jobject __unused obj,
        jint value
) {
    player->setPitchShift(value);
}
```
Check out in full: https://github.com/peteee/SuperpoweredPlayer/blob/master/app/src/main/cpp/PlayerExample.cpp


## What is Superpowered C++ Audio Library and SDK for Android, iOS, macOS, tvOS, Linux and Windows?
Check it out here: https://superpowered.com

Superpowered C++ Audio Library and SDK is the leading C++ Audio Library featuring low-power, real-time latency and cross-platform audio players, audio decoders, Fx (effects), audio I/O, streaming, music analysis and spatialization.

For the most up-to-date feature list, see: https://superpowered.com/audio-library-sdk

### NOTE: the Superpowered SDK is not included! This example uses Superpowered Audio SDK version 1.3.1
#### Download it from here: https://github.com/superpoweredSDK/Low-Latency-Android-iOS-Linux-Windows-tvOS-macOS-Interactive-Audio-Platform






