# CreuCatPet-ReconstructionProject
[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/stabledsteak2/CreuCatPet-ReconstructionProject)

This repository contains the source code and documentation for the CreuCatPet Reconstruction Project. The project focuses on developing, implementing, and evaluating algorithms for medical image reconstruction, with a primary emphasis on data from Positron Emission Tomography (PET) and Computed Tomography (CT) scanners.

## Overview

Image reconstruction is the process of forming a viewable image from the raw data produced by a medical imaging scanner. This project provides a framework for experimenting with various reconstruction techniques. The goal is to create a modular and extensible platform for researchers and developers working in the field of medical physics and imaging.

### Key Goals
*   **Implement Standard Algorithms:** Provide robust implementations of well-known reconstruction algorithms such as Filtered Back-Projection (FBP), Maximum Likelihood Expectation Maximization (MLEM), and Ordered Subsets Expectation Maximization (OSEM).
*   **Data Handling:** Support common medical imaging data formats for raw (sinogram) and reconstructed (image) data.
*   **Modularity:** Design a flexible architecture that allows for easy integration of new reconstruction algorithms, correction steps (e.g., attenuation, scatter), and data sources.
*   **Performance:** Optimize critical code paths for performance, leveraging parallel computing where applicable.

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

This project requires Python 3.8+ and several scientific computing libraries. It is recommended to use a virtual environment.

*   Python 3.8+
*   pip

### Installation

1.  Clone the repository:
    ```sh
    git clone https://github.com/stabledsteak2/CreuCatPet-ReconstructionProject.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd CreuCatPet-ReconstructionProject
    ```
3.  Install the required Python packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

The primary way to use the software is through the command-line interface. You can run a reconstruction using the `reconstruct.py` script.

### Example

To run a reconstruction using the OSEM algorithm on a specified input data file, use the following command:

```sh
python reconstruct.py --input /path/to/your/sinogram_data.hs --output /path/to/reconstructed_image.img --algorithm OSEM --iterations 10 --subsets 8
```

**Command-Line Arguments:**
*   `--input`: Path to the raw input data (sinogram).
*   `--output`: Path where the reconstructed image will be saved.
*   `--algorithm`: The reconstruction algorithm to use (e.g., `FBP`, `MLEM`, `OSEM`).
*   `--iterations`: (For iterative algorithms) The number of iterations to perform.
*   `--subsets`: (For OSEM) The number of subsets to use.

For a full list of options and their descriptions, run:
```sh
python reconstruct.py --help
```

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## License

This project is distributed under the MIT License. See the `LICENSE` file for more information.
