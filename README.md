# ND2-Timelapse-Visualizer
Jupyter notebook containing python codes to process multidimensional ND2 images and export them as timelapse videos. [Version:1]

### Read Me
This notebook automates the processing of raw Nikon ND2 microscopy files into presentation-ready video files. It is designed to handle multi-dimensional data containing Time (T), Z-stacks (Z), Multi-positions (S), and Channels (C).
#### Key Features
- Metadata Extraction: Automatically reads physical dimensions (x, y, z) and time intervals (t).
- Z-Projection: Converts 3D stacks into 2D images using Maximum Intensity Projection (MIP).
- Auto-Normalization: Applies percentile-based normalization to enhance contrast while ignoring hot pixels.
- Custom Visualization: Applies user-defined colormaps (LUTs) to specific channels.
- Automatic Annotation:
    - Scale Bar: Draws a physical scale bar based on metadata pixel size.
    - Timestamp: Calculates and stamps "HH:MM" on every frame based on acquisition intervals.
- Export: Saves individual channels and merged overlays as .mp4 video files.
- Batch Processing: Can process a single file or iterate through an entire directory.

#### How to Use
1. Input Data: Place your .nd2 files in a local directory.
2. Configuration (Section 3): Update the WorkingDir path to your folder.
3. Channel Mapping: Update the ChannelInfo dictionary to match your specific experiment (e.g., Channel 0 = "DAPI", Color = "Blue").
4. Run: Execute all cells. The script will create a _Processed folder containing the output videos.
