# Feature Matching Benchmark Results

Comparison of **ORB** and **SIFT** algorithms across five image transformation categories.

---

## Rotation

| Algorithm | Test | Similarity Score | Robustness | Time | Unmatched KP | Good Matches | # KP |
|-----------|------|-----------------|------------|------|--------------|--------------|------|
| ORB | rotate1 | 0.65 | 0.976 | 0.0595 sec | 732 | 650 | 1000 |
| ORB | rotate2 | 0.60 | 0.991 | 0.0582 sec | 818 | 605 | 1000 |
| ORB | rotate3 | 0.57 | 0.989 | 0.0932 sec | 874 | 575 | 1000 |
| SIFT | rotate1 | 0.63 | 0.963 | 0.5868 sec | 754 | 632 | 1000 |
| SIFT | rotate2 | 0.62 | 0.964 | 0.4109 sec | 766 | 625 | 1000 |
| SIFT | rotate3 | 0.61 | 0.954 | 0.4227 sec | 801 | 611 | 1000 |

---

## Blur

| Algorithm | Test | Similarity Score | Robustness | Time | Unmatched KP | Good Matches | # KP |
|-----------|------|-----------------|------------|------|--------------|--------------|------|
| ORB | blur1 | 0.61 | 0.990 | 0.0629 sec | 816 | 612 | 1000 |
| ORB | blur2 | 0.36 | 0.969 | 0.2338 sec | 1306 | 362 | 1000 |
| ORB | blur3 | 0.29 | 0.715 | 0.0408 sec | 1195 | 123 | 424 |
| SIFT | blur1 | 0.374 | 0.943 | 0.4147 sec | 1270 | 374 | 1000 |
| SIFT | blur2 | 0.393 | 0.879 | 0.3936 sec | 1440 | 232 | 1000 |
| SIFT | blur3 | 0.31 | 0.721 | 0.3411 sec | 1138 | 104 | 1000 |

Image example, features matching

ORB:

<img width="948" height="360" alt="image" src="https://github.com/user-attachments/assets/85ced664-8076-4c2c-b705-dbd61c6f94d4" />

SIFT:

<img width="942" height="351" alt="image" src="https://github.com/user-attachments/assets/ff3c87c0-d1b7-4dfc-b8a9-6ab4ee6c9cbf" />

---

## Viewpoint Change

| Algorithm | Test | Similarity Score | Robustness | Time | Unmatched KP | Good Matches | # KP |
|-----------|------|-----------------|------------|------|--------------|--------------|------|
| ORB | VP1 | 0.56 | 0.976 | 0.0607 sec | 930 | 563 | 1000 |
| ORB | VP2 | 0.35 | 0.988 | 0.0568 sec | 1342 | 352 | 1000 |
| ORB | VP3 | 0.13 | 0.963 | 0.0570 sec | 1742 | 138 | 1000 |
| SIFT | VP1 | 0.656 | 0.948 | 0.4191 sec | 716 | 656 | 1000 |
| SIFT | VP2 | 0.511 | 0.933 | 0.6507 sec | 1002 | 511 | 1000 |
| SIFT | VP3 | 0.232 | 0.875 | 0.4035 sec | 1553 | 232 | 1000 |

---

## Lighting

| Algorithm | Test | Similarity Score | Robustness | Time | Unmatched KP | Good Matches | # KP |
|-----------|------|-----------------|------------|------|--------------|--------------|------|
| ORB | light1 | 0.87 | 0.995 | 0.0626 sec | 283 | 874 | 1000 |
| ORB | light2 | 0.88 | 0.995 | 0.0603 sec | 242 | 889 | 1000 |
| ORB | light3 | 0.53 | 0.981 | 0.0884 sec | 961 | 533 | 1000 |
| SIFT | light1 | 0.83 | 0.981 | 0.4066 sec | 357 | 832 | 1000 |
| SIFT | light2 | 0.82 | 0.986 | 0.4233 sec | 356 | 829 | 1000 |
| SIFT | light3 | 0.51 | 0.946 | 0.3599 sec | 992 | 515 | 1000 |

---

## Salt-and-Pepper Noise

| Algorithm | Test | Similarity Score | Robustness | Time | Unmatched KP | Good Matches | # KP |
|-----------|------|-----------------|------------|------|--------------|--------------|------|
| ORB | SP1 | 0.55 | 0.987 | 0.1020 sec | 926 | 557 | 1000 |
| ORB | SP2 | 0.30 | 0.957 | 0.1279 sec | 1409 | 308 | 1000 |
| ORB | SP3 | 0.21 | 0.926 | 0.0789 sec | 1594 | 218 | 1000 |
| SIFT | SP1 | 0.80 | 0.975 | 0.4079 sec | 427 | 800 | 1000 |
| SIFT | SP2 | 0.22 | 0.830 | 0.6999 sec | 1573 | 224 | 1000 |
| SIFT | SP3 | 0.09 | 0.785 | 0.3850 sec | 1813 | 98 | 1000 |

Image example of key points detection ORB:

<img width="1723" height="640" alt="image" src="https://github.com/user-attachments/assets/5b555422-9098-48f6-a562-46ae966a05bb" />


---

## Summary (Averages per Transformation)



<img width="1328" height="309" alt="image" src="https://github.com/user-attachments/assets/68de668b-844f-4524-b2a1-178deae09c63" />

M-KP -> is shortage for matched key points


Conclusion: it is obvious that ORB is way faster than SIFT, yet for the performance it depends on the task, in general the performance of SIFT is better.


Data Reference: https://www.kaggle.com/datasets/muratiik/a-data-set-to-compare-feature-extractors/data
