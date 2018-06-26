add_executable(HelloEngine_Win_d2d WIN32 helloengine_win_d2d.cpp)
target_link_libraries(HelloEngine_Win_d2d user32.lib ole32.lib d2d1.lib)