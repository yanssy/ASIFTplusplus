# ASIFT++:
Descriptor based on SIFT which is robust to *out-of-plane* rotations. ASIFT properly deals only with in-plane rotations. I used OpenCV implementation of SIFT. 

# Robust to in-plane rotation alghoritm (ASIFT):
http://www.cmap.polytechnique.fr/~yu/research/ASIFT/demo.html

# Adapted 3D reconstruction alghoritm:
http://cvlab.epfl.ch/files/content/sites/cvlab2/files/publications/publications/2012/OstlundVF12.pdf

# BUILD:
- build using standard procedure (mkdir build -> cd build -> cmake .. -> make)
- in _build_ folder prepare folder _images_ and create here _chessboard.txt_ wher you list all your chessboard files (needed for initial deformation) - examplary images are in _images_ folder from this repo.
- Paste to _build_ folder all files from dataset (EPFL): cam.ext, cam.intr, cam.tdir, ControlPointIds.txt, im_corners.txt, mesh.pts, mesh.tri, webcam.intr, world_corners.txt
- Usage: ./affineDSC path_to_model.png path_to_frame.png detector descriptor ratio1% ratio2% isPointCloudSaved(0 / 1)

# RESULTS:
- All matches found:
![All matches found](https://raw.githubusercontent.com/mbed92/ASIFTplusplus/master/PC_056_80_90_sift_sift_all.png)

- Displacement of added keypoints:
![Displacement of improved keypoints](https://raw.githubusercontent.com/mbed92/ASIFTplusplus/master/PC_056_80_90_sift_sift_disp.png)

- Position of added keypoints:
![Added matches](https://raw.githubusercontent.com/mbed92/ASIFTplusplus/master/PC_056_80_90_sift_sift_imp.png)
