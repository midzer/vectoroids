# Emscripten

## Build and link

emcc -flto -O3 *.c -o index.html -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sSDL2_IMAGE_FORMATS='["jpg"]' -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["mod","wav"]' -sASYNCIFY -sASYNCIFY_ONLY=["main","SDL_Delay","GLES2_RenderPresent","Emscripten_GLES_SwapWindow","dynCall_v"] -sASYNCIFY_IGNORE_INDIRECT -sENVIRONMENT=web -sINITIAL_MEMORY=128MB --preload-file data/ -Wl,-u,fileno --closure 1
