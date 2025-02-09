# GPU Conditional Rendering Strategies

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://doliveira4.github.io/gpuconditionals/) 
![WebGPU Required](https://img.shields.io/badge/WebGPU-required-blue)

Experimental implementation comparing GPU conditional evaluation strategies, based on [Íñigo Quílez's analysis](https://iquilezles.org/articles/gpuconditionals/).

## Key Features
- Branching (`if/else`) vs branchless (`step/mix`) implementations
- Real-time threshold control with animated feedback
- WebGPU-powered rendering pipeline
- Performance comparison framework

## Installation & Usage
```
git clone https://github.com/doliveira4/gpuconditionals.git
cd gpuconditionals
python -m http.server 8000
```

Open `http://localhost:8000` in **Chrome 113+** with WebGPU enabled via:
1. Navigate to `chrome://flags/#enable-unsafe-webgpu`
2. Enable flag and restart

## Controls
| Control | Purpose | Range |
|---------|---------|-------|
| Conditional Type | Switch between implementations | 0-1 |
| Threshold Slider | Adjust decision boundary | 0-1 |

## Technical Implementation
- **Buffer Management**: Minimal 12-byte uniform buffer
- **Shader Design**: Dual-path WGSL shader with dynamic branching
- **Animation Loop**: Time-based threshold modulation for visual feedback

## Results Analysis
Use Chrome DevTools to profile:
1. Open Performance tab
2. Record while toggling modes
3. Compare frame timing and GPU load

## Contributing
PRs welcome! Please follow:
- Atomic commits
- WebGPU best practices
- Clear shader comments

## License
Free for non-commercial use © 2025 David Oliveira
