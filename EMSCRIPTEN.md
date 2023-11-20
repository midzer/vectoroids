# Emscripten

## Compile

emcc -flto -O3 vectoroids.c -c -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sUSE_SDL_MIXER=2

## Link

emcc -flto -O3 *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_IMAGE=2 -sSDL2_IMAGE_FORMATS='["jpg"]' -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["mod","wav"]' -sASYNCIFY -sENVIRONMENT=web --preload-file data/ -Wl,-u,fileno --closure 1
