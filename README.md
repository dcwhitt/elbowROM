# Elbow ROM Tracker

A browser-based point-and-click tool for measuring elbow flexion, extension deficit, and arc of motion from lateral elbow photos.

The tool supports both:

- Taking a new photo with the device camera
- Uploading an existing photo

This project is designed to begin as a fully manual measurement tool and later support pose-estimation or machine-learning-assisted landmark detection.

## Project Goal

The goal is to create a simple clinical/research tool that can estimate elbow range of motion from lateral images.

The app allows users to:

- Take or upload a flexion photo
- Take or upload an extension photo
- Manually click an upper-arm point, elbow center, and forearm/wrist point
- Calculate elbow angle
- Calculate extension deficit
- Calculate arc of motion
- Export marked images
- Export CSV results
- Export JSON landmark labels for future model training

## Current Version

**Version:** `0.1.0-manual`

This version is fully manual. No machine learning or automated pose tracking is currently used.

## Measurement Workflow

For each image, the user clicks three landmarks:

1. Proximal humerus / upper-arm point
2. Elbow center
3. Distal forearm / wrist point

The app calculates the angle at the elbow between:

- Humerus axis
- Forearm axis

## Outputs

The app can export:

- Marked flexion image
- Marked extension image
- CSV measurement summary
- JSON landmark labels
- Full case JSON file

## ROM Calculations

The app stores the raw elbow angle for each image.

For extension:

```text
extension_deficit = 180 - extension_angle
