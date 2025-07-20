# ISB-2025 Shape Modeling Tutorial

**Neural Shape Models: Learning Implicit Representations with Signed Distance Functions**

This repository contains hands-on tutorials for learning neural implicit surface representations using Signed Distance Functions (SDFs). Developed for the International Society of Biomechanics (ISB) 2025 conference, these tutorials demonstrate how to use deep learning to create continuous, differentiable representations of 3D medical imaging data.

## 🎯 What You'll Learn

- **Signed Distance Functions (SDFs)**: Understand implicit surface representations
- **Neural Implicit Networks**: Train MLPs to learn coordinate-to-SDF mappings  
- **Medical Imaging Applications**: Work with real tibia bone meshes from medical scans
- **Surface Reconstruction**: Extract surfaces using marching cubes algorithm
- **PyTorch Implementation**: Hands-on deep learning with practical examples

## 📚 Tutorials

> **How to enable GPU in Google Colab:**
>
> 1. Open the Colab notebook.
> 2. Click the arrow next to the `Connect` button (top right).
> 3. Select **Change runtime type**.
> 4. Under "Hardware accelerator", choose **T4 GPU**.
> 5. Click **Save**.

**Colab Notes:**
- Libraries are installed automatically.
- You may need to click "Restart runtime" after installation for changes to take effect.
- After restarting, continue running the notebook as usual.

### Tutorial 1: SDF Fundamentals
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gattia/ISB-2025-Shape-Modeling/blob/main/1_SDF_Tutorial.ipynb)

Learn the basics of Signed Distance Functions and train your first neural implicit representation:

- 🔹 **SDF Theory**: What are signed distance functions and why use them?
- 🔹 **Data Preparation**: Smart sampling strategies for training data generation  
- 🔹 **Network Design**: MLP architecture for coordinate-to-SDF learning
- 🔹 **Training Process**: Optimization strategies and loss functions
- 🔹 **Visualization**: See your learned SDF field and reconstructed surfaces
- 🔹 **Surface Extraction**: Use marching cubes to get explicit mesh representations

### Tutorial 2: Advanced Shape Modeling
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gattia/ISB-2025-Shape-Modeling/blob/main/2_Generative_SDF_Tutorial.ipynb)

Build generative models that can represent multiple bone shapes and generate new variations:

- 🔹 **Generative SDFs**: Learn one network to represent multiple bone shapes
- 🔹 **Latent Embeddings**: Use learnable shape codes to encode bone identity  
- 🔹 **Multi-Shape Training**: Register and normalize datasets from multiple patients
- 🔹 **Shape Space Exploration**: Generate average bones using latent arithmetic
- 🔹 **Generative Modeling**: Interpolate between shapes and create novel variations
- 🔹 **Medical Applications**: Population analysis and statistical shape modeling

## 🚀 Quick Start

### Option 1: Google Colab (Recommended)
1. Click the Colab badge above for Tutorial 1
2. Run the cells sequentially - all dependencies will be installed automatically
3. Note: Some 3D visualizations may have limited interactivity in Colab

### Option 2: Local Setup
```bash
# Clone the repository
git clone https://github.com/gattia/ISB-2025-Shape-Modeling.git
cd ISB-2025-Shape-Modeling

# create an environment. E.g., 
conda create -n isb_tutorial
# Install dependencies (recommend using conda/mamba)
pip install torch torchvision pymskt pyvista itkwidgets matplotlib numpy jupyter

```

## 📁 Repository Structure

```
ISB-2025-Shape-Modeling/
├── 1_SDF_Tutorial.ipynb          # Tutorial 1: SDF Fundamentals  
├── list_meshes.json              # List of available mesh files
├── data/                         # Medical imaging data
│   ├── 9226874_LEFT_tibia.vtk   # Example tibia meshes
│   ├── 9226874_RIGHT_tibia.vtk  # (Multiple subjects/sides)
│   ├── ...                      # Additional mesh files
└── README.md                     # This file
```

## 🔧 Dependencies

**Core Libraries:**
- `torch` - Deep learning framework
- `pymskt` - Medical imaging toolkit for mesh operations  
- `pyvista` - 3D data processing and visualization
- `numpy` - Numerical computing
- `matplotlib` - Plotting

**Interactive Visualization:**
- `itkwidgets` - 3D visualization in Jupyter (may have limited functionality in Colab)

**Note for Colab Users:** All dependencies will be automatically installed when you run the first cell. Some 3D visualizations may render differently in Colab compared to local Jupyter environments.

## 📊 Data

The tutorial uses real medical imaging data from tibia bone reconstructions. The meshes are stored in VTK format and include:

- **Multiple subjects**: Different bone shapes and sizes
- **Left/Right bones**: Anatomical variation examples  
- **High-quality meshes**: Suitable for learning detailed surface representations

*Data source: Medical imaging reconstructions processed for educational use*

## 🤝 Getting Help

- **Issues**: Found a bug or have a question? [Open an issue](https://github.com/gattia/ISB-2025-Shape-Modeling/issues)
- **Discussions**: Want to share results or ask questions? Use the [Discussions tab](https://github.com/gattia/ISB-2025-Shape-Modeling/discussions)

## 📖 Background

Neural implicit representations are revolutionizing how we work with 3D data:

- **Traditional approaches**: Explicit meshes, voxel grids (fixed resolution, memory intensive)
- **Neural implicit**: Continuous surfaces encoded in network weights (compact, differentiable)
- **Applications**: Computer graphics, medical imaging, 3D AI, shape analysis

This tutorial bridges the gap between theory and practice, giving you hands-on experience with cutting-edge techniques used in research and industry.

## 📄 Citation

If you use these tutorials in your research or educational work, please cite:

```bibtex
@misc{gatti2025isbshapemodeling,
  title={ISB-2025 Shape Modeling Tutorial: Neural Implicit Representations with SDFs},
  author={Gatti, Anthony A., Clouthier, A., Lee, E., Rainbow M.},
  year={2025},
  url={https://github.com/gattia/ISB-2025-Shape-Modeling}
}
```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Ready to start learning?** Click the Colab badge above and dive into Tutorial 1! 🚀 


## 🛠️ Development Notes

- **Clear Notebook Outputs Before Commit:**  
  To keep the repository lightweight and ensure fast loading in Colab, please clear all cell outputs from the notebooks before committing changes. You can do this with:
  ```
  jupyter nbconvert --clear-output --inplace <notebook_name>.ipynb
  ```
  This helps prevent large file sizes and unnecessary output clutter in version control.
