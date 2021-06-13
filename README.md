# spot-img-diff

Very primitive demo how to compare 2 screenshots of webpage. These screenshots can be misaligned especially on y-axis due to scrolling up/down on websites. 

This demo can:
- align sreenshots in any direction using homography based on opencv feature matching (however this can sometime produce noise)
- align screenshots only in vertical direction using calculated median shift in matched keypoints (this limits the noise to absolute minimum)
- detect difference between aligned webpages and visualize bounding box (using closing operation in horizontal direction ensures the bounding box captures the whole row of difference)
- Experimental: Read and compare text difference within detected bounding box

## References

- https://arxiv.org/pdf/1808.10584.pdf
- https://github.com/madmaze/pytesseract
- https://tesseract-ocr.github.io/tessdoc/#introduction
- https://stackoverflow.com/questions/17566752/how-to-find-subimage-using-the-pil-library
- https://learnopencv.com/feature-based-image-alignment-using-opencv-c-python/
- https://testing.googleblog.com/2011/10/unleash-qualitybots.html
- https://www.pyimagesearch.com/2017/06/19/image-difference-with-opencv-and-python/