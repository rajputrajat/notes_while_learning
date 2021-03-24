# Webgpu

going through following video:
`https://www.youtube.com/watch?v=EhWvqaRDz5s&t=3s`

## WebGL

**** webGL is java api

## advantages of WebGPU over WebGL

. better cpu performance
. access to GPU compute functionality
. factors cost at loading time -> better cpu perf
. views the GPU as commands
. in Scene Graph, divide nodes in static and dynamic nodes
. allow reused of commands. create bundles
. precompute static commands for bundle
. use that precompute bundle later -> no computation needed at draw in this way
. babylon js demonstation show almost negligble usage of cpu compared to WebGL
. efficient with compute shaders

### implementation for WebGPU

* Dawn Wire at web side in js
* on web js part and GPU side run in separate processes
* other side is called Dawn Native, this talks to DX12, Vulkan, Metal APIs
* native apps can directly use Dawn Native apis
* of wgpu-rs :-)
* use wasm
