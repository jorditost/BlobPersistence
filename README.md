Blob Persistence
================

This repository contains an implementation of [this](http://shiffman.net/2011/04/26/opencv-matching-faces-over-time/) blob persistence algorithm by Daniel Shiffman using the [OpenCV library for Processing](https://github.com/atduskgreg/opencv-processing) by Greg Borenstein.

## Following blobs over time

For some applications it may be important to "follow" a blob or an object over time (as markers or TUIO do).

> "One of the most common questions I get regarding blob tracking is “memory.” How do I know which blob is which over time? Computer vision libraries, for the most part, simply pass you a list of blobs (with x, y, width, and height properties) for any given moment in time. But the blobs themselves represent only a snapshot of that particular moment and contain no information related to whether the blobs existed before this very moment. This may seem absurd given that as human beings it’s so easy for us to watch a rectangle moving across a screen and understand conceptually that it is the same rectangle. But without additional information (such as color matching, an AR marker, etc.) there’s no way for an algorithm that analyzes one frame of video to know anything about a previous frame. And so we need to apply the same intuitions our brain uses (it was there a moment ago, it’s probably still there now) to our algorithms" (by [Daniel Shiffman](http://shiffman.net/2011/04/26/opencv-matching-faces-over-time/))

## Face memory

The sketch [WhichFace](https://github.com/jorditost/BlobPersistence/tree/master/WhichFace) implements a persistence algorithm that follows faces over time. It is a modification of Daniel Shiffman's algorithm to work with the [OpenCV library for Processing](https://github.com/atduskgreg/opencv-processing) by Greg Borenstein (the [original code](http://shiffman.net/p5/whichface.zip) works with another -older- implementation of OpenCV)

![](WhichFace/screenshots/whichface.png)

Code:
- [WhichFace.pde](https://github.com/jorditost/BlobPersistence/blob/master/WhichFace/WhichFace.pde): main sketch
- [Face.pde](https://github.com/jorditost/BlobPersistence/blob/master/WhichFace/Face.pde): the Face class

To see a detailed information of this algorithm visit Daniel Shiffman's blog:
http://shiffman.net/2011/04/26/opencv-matching-faces-over-time/