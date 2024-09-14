cmake_minimum_required(VERSION 3.22)
project(soloudw)

set(CMAKE_CXX_STANDARD 23)
set(HEADERS
	include/soloudw/soloud.h
	include/soloudw/soloud_audiosource.h
	include/soloudw/soloud_ay.h
	include/soloudw/soloud_bassboostfilter.h
	include/soloudw/soloud_biquadresonantfilter.h
	include/soloudw/soloud_bus.h
	include/soloudw/soloud_c.h
	include/soloudw/soloud_dcremovalfilter.h
	include/soloudw/soloud_duckfilter.h
	include/soloudw/soloud_echofilter.h
	include/soloudw/soloud_eqfilter.h
	include/soloudw/soloud_error.h
	include/soloudw/soloud_fader.h
	include/soloudw/soloud_fft.h
	include/soloudw/soloud_fftfilter.h
	include/soloudw/soloud_file.h
	include/soloudw/soloud_file_hack_off.h
	include/soloudw/soloud_file_hack_on.h
	include/soloudw/soloud_filter.h
	include/soloudw/soloud_flangerfilter.h
	include/soloudw/soloud_freeverbfilter.h
	include/soloudw/soloud_internal.h
	include/soloudw/soloud_lofifilter.h
	include/soloudw/soloud_misc.h
	include/soloudw/soloud_monotone.h
	include/soloudw/soloud_noise.h
	include/soloudw/soloud_openmpt.h
	include/soloudw/soloud_queue.h
	include/soloudw/soloud_robotizefilter.h
	include/soloudw/soloud_sfxr.h
	include/soloudw/soloud_speech.h
	include/soloudw/soloud_tedsid.h
	include/soloudw/soloud_thread.h
	include/soloudw/soloud_vic.h
	include/soloudw/soloud_vizsn.h
	include/soloudw/soloud_wav.h
	include/soloudw/soloud_waveshaperfilter.h
	include/soloudw/soloud_wavstream.h
	include/soloudw/zx7decompress.h)
set(SOURCES 
    src/dr_impl.cpp 
    src/soloud.cpp 
    src/soloud_audiosource.cpp 
    src/soloud_bus.cpp 
    src/soloud_core_3d.cpp 
    src/soloud_core_basicops.cpp 
    src/soloud_core_faderops.cpp 
    src/soloud_core_filterops.cpp 
    src/soloud_core_getters.cpp 
    src/soloud_core_setters.cpp 
    src/soloud_core_voicegroup.cpp 
    src/soloud_core_voiceops.cpp 
    src/soloud_fader.cpp 
    src/soloud_fft.cpp 
    src/soloud_fft_lut.cpp 
    src/soloud_file.cpp 
    src/soloud_filter.cpp 
    src/soloud_miniaudio.cpp 
    src/soloud_misc.cpp 
    src/soloud_queue.cpp 
    src/soloud_thread.cpp 
    src/soloud_wav.cpp 
    src/soloud_wavstream.cpp 
    src/stb_vorbis.c)
set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

add_compile_definitions(WITH_MINIAUDIO)
add_library(soloudw ${HEADERS} ${SOURCES})
target_include_directories(soloudw PUBLIC include/soloudw)
