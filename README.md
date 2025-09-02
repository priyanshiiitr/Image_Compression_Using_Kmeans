# Image Compression Using K-means

A Python implementation of the K-means clustering algorithm from scratch, applied to image compression. This project demonstrates how K-means can reduce the number of colors in an image while maintaining visual quality[web:1].

## 🎯 Overview

This project implements the K-means clustering algorithm to compress images by reducing their color palette. Instead of using thousands of colors, the compressed image uses only 16 representative colors, significantly reducing storage requirements while preserving the essential visual characteristics[web:2].

## 🔍 How It Works

The image compression process works by:

1. **Color Space Representation**: Each pixel in the original image is treated as a 3D data point in RGB space  
2. **Clustering**: K-means algorithm groups similar colors together into 16 clusters  
3. **Centroid Calculation**: Each cluster's centroid represents the optimal color for that group  
4. **Color Replacement**: All pixels in a cluster are replaced with their centroid color  
5. **Reconstruction**: The compressed image is reconstructed using only the 16 representative colors[web:2].

## 📁 Project Structure

Image_Compression_Using_Kmeans/
├── k_means_and_image_cpmpression.ipynb # Main implementation notebook
├── sample.png # Sample image for compression
└── README.md # This file


## 🚀 Features

- **From-scratch implementation** of K-means clustering algorithm[web:2]
- **Complete workflow** from initialization to convergence
- **Visual comparison** between original and compressed images
- **Detailed documentation** with mathematical explanations
- **Modular functions** for easy understanding and reuse

## 🛠 Implementation Details

### Core Functions

1. **`find_closest_centroids(X, centroids)`**
   - Assigns each data point to its nearest centroid
   - Uses L2-norm (Euclidean distance) for distance calculation

2. **`compute_centroids(X, idx, K)`**
   - Recalculates centroid positions based on assigned points
   - Updates centroids as the mean of assigned data points

3. **`run_Kmeans(X, initial_centroids, max_iters)`**
   - Main K-means algorithm orchestrator
   - Iteratively refines clusters until convergence

4. **`kMeans_init_centroids(X, K)`**
   - Randomly initializes centroids from the dataset
   - Prevents duplicate centroid selection[web:2]

## 📊 Algorithm Steps

1. **Initialization**: Randomly select K initial centroids
2. **Assignment**: Assign each pixel to the closest centroid
3. **Update**: Recalculate centroids as the mean of assigned pixels
4. **Iteration**: Repeat steps 2-3 until convergence
5. **Compression**: Replace original colors with centroid colors

## 🎨 Results

The algorithm successfully compresses images by:
- Reducing color palette from thousands to 16 colors
- Maintaining visual similarity to the original image
- Achieving significant file size reduction
- Demonstrating the power of unsupervised learning[web:2]

## 🔧 Requirements


## 📖 Usage

1. **Load the notebook**: Open `k_means_and_image_cpmpression.ipynb`
2. **Run all cells**: Execute the notebook from top to bottom
3. **View results**: Compare original and compressed images
4. **Experiment**: Try different values of K (number of clusters)[web:2]

## 🔬 Technical Details

### Mathematical Foundation

The K-means algorithm minimizes the within-cluster sum of squares:


Where:
- `x(i)` is the i-th data point (pixel RGB values)
- `μ(c(i))` is the centroid of the cluster assigned to x(i)
- `c(i)` is the cluster assignment for point i

### Compression Efficiency

- **Original**: 24-bit color (8 bits × 3 channels = 24 bits per pixel)
- **Compressed**: 4-bit index + color palette (4 bits per pixel + 16 × 24 bits)
- **Compression ratio**: Approximately 6:1 for typical images[web:2]

## 🚀 Future Enhancements

- [ ] **K-means++**: Implement smarter centroid initialization
- [ ] **Elbow method**: Automatic K selection
- [ ] **Different color spaces**: LAB, HSV color space compression
- [ ] **Performance optimization**: Vectorized operations
- [ ] **Quality metrics**: PSNR, SSIM evaluation
- [ ] **Interactive interface**: GUI for real-time compression

## 🎓 Learning Objectives

This project demonstrates:
- Unsupervised machine learning concepts
- K-means clustering algorithm implementation
- Image processing and manipulation
- NumPy array operations and vectorization
- Data visualization with matplotlib[web:2]

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Add new features or optimizations
- Improve documentation
- Fix bugs or issues
- Add more test images

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Priyanshi**  
- GitHub: [@priyanshiiitr](https://github.com/priyanshiiitr)

---

⭐ **Star this repository if you found it helpful!**
