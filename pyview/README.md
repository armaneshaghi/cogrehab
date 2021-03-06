PyView
======

This module tries to imitate Freeview, which is a 
C++ package for visualisation of Freesurfer outputs.
PyView is designed to work inside IPython notebook only, 
makes use of advanced visualization and interactive widgets
inside IPython notebook. Therefore, using it outside IPython
notebook fails.

Warning: This package is constantly changing and unreleased. 

---

Example usage:

```python
from cogpy.pyview import mri
slices = np.zeros([4, 3])
slices[0,0] = 128
slices[1,0] = 118
slices[2,0] = 100
slices[3,0] = 90
slices[0,1] = 128
slices[1,1] = 100
slices[2,1] = 40
slices[3,1] = 128
slices[0,2] = 100
slices[1,2] = 90
slices[2,2] = 128
slices[3,2] = 100
fscheck = mri.FS(subject_name = 'baseline_V_V1', slices = slices)
fscheck.superimpose()
```

The output inside IPython notebook shows pial surface in yellow and white matter surface in red:
 
![alt text](pyview_example.png "surface on volume overlay")

