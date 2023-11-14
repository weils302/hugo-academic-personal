---
title: Digital Office Door Sign Update Log
subtitle: 

# Summary for listings and search engines
summary: Version Updated Record

# Link this post with a project
projects: [digital_office_door_sign]

# Date published
date: '2023-04-20T00:00:00Z'

# Date updated
lastmod: '2023-05-10T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ''
  placement: 2
  preview_only: true

authors:
  - WEILISI

tags:
  - Digital Office Door Sign
  - AI

categories:
  - Tech Blog
---

### V2.0.0: Added a service stop button and implemented an automatic image switching feature （2023.5.10）
---
<div style="text-align: justify;">
Previously, changing the status required accessing VNC Viewer, pressing ESC to exit the image display, then selecting a new status. 
This process was somewhat cumbersome, so in this version, it has been changed to automatically switch images by clicking the 
"Set Status" button. This function will disable the ESC key, preventing control of the Raspberry Pi via VNC Viewer. 
To address this, some code logic has been revised, and a service stop button has been added. 
The functionality of the service stop button is equivalent to that of the ESC key in previous versions.
</div>

![V2.0.0](V2.0.0.png)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">V2.0.0 client window, with the addition of the "Shutdown Server" button.</p>


### V1.1.0: Added "Lecture" status, fixed display issues (2023.4.25)  
---
<div style="text-align: justify;">
As "Lecture" is a frequently used status, a corresponding option has been added. Moreover, in the previous version, 
images appeared to be automatically enlarged, leading to the edges of the images not being displayed. 
This issue has been resolved in this update.
</div>

![lecture](lecture.jpg)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">One of the images for the "Lecture" status</p>

![V1.1.0](V1.1.0.png)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">V1.1.0 client window, with the addition of the "Lecture" option.</p>

![margin](margin.jpg)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">Fixed the issue of image edges being cropped.</p>


### V1.0.0: Product officially put into use (2023.4.20)
---
<div style="text-align: justify;">
The first version has been deployed. It allows users to select and set their in-room status for different weather conditions
(as it is currently spring, the snowy weather feature is not available). The status can be set through the steps of "selecting → clicking the set status button."
To set the next status, one needs to press ESC in VNC Viewer to exit the image display before setting the status.
</div>

![V1.0.0](V1.0.0.png)
<p style="font-size: 16px; line-height: 1.6; text-align: center;">V1.0.0 client window.</p>
