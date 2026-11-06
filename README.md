# Segmenting the Heart from Cardiac MRI

How well can you outline the right atrium of the heart by hand from MRI scans, and how do you measure "well"?

**Individual coursework · Processing and Analysis in Medical Imaging · Queen Mary University of London, 2024–25**

## What I did

Using public cardiac MRI data from the Atrial Segmentation Challenge Dataset, I segmented the right atrium by hand in 3D Slicer, adjusting intensity thresholds and refining the outline slice by slice. I then exported the segmentation and used MATLAB to compare it against the gold-standard segmentation, calculating precision, recall and the Dice score.

## What went wrong

My precision looked excellent at first: almost everything I marked as right atrium really was. But the recall showed I had missed a large part of it, especially around the boundaries. It was a good lesson in not trusting a single metric. Precision on its own made the segmentation look far better than it was.

## Results

- Precision: **91.65%**
- Recall: **41.77%**
- Dice score: **0.574**

The segmentation matched the gold standard well visually, with most of the disagreement at the edges of the atrium.

![3D Slicer segmentation](https://raw.githubusercontent.com/yemesis/medical-imaging-analysis/main/figures/3d-slicer-ra-segmentation.png)

![Segmentation vs gold standard](https://raw.githubusercontent.com/yemesis/medical-imaging-analysis/main/figures/segmentation-vs-gold-standard.png)

![Segmentation performance](https://raw.githubusercontent.com/yemesis/medical-imaging-analysis/main/figures/segmentation-performance.png)

## Tools

3D Slicer · MATLAB

## Files

- [Full report](./medical-imaging-analysis-report.pdf)
