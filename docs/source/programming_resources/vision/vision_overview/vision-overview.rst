Computer Vision Overview
========================

Introduction
------------

The *FIRST* Tech Challenge control system software has built-in support for two
computer vision technologies:

1.AprilTags -
   :doc:`AprilTags <../../../apriltag/vision_portal/apriltag_intro/apriltag-intro>`
   are fiducial markers similar in design to a QR code that can be used
   for identification and localization. AprilTags are used as reference 
   points for autonomous navigation and for assisted navigation and
   identification of points of interest on a game field.

   -  Each season, FIRST provides 2D image targets that can be used as
      navigational reference points.
   -  If the AprilTag system recognizes an AprilTag image, it provides 
      very accurate pose information (assuming the camera used has 
      calibration parameters for the working resolution) about the 
      robot’s position relative to the target.
   -  A robot can use this information to navigate autonomously on the
      field.
2. Color Processing - :doc:`Color Processing <../../../color_processing/index>`
   uses the OpenCV library that is built in to the FTC SDK to locate regions
   of certain colors or determine the color of a certain region. This can be
   useful for finding game elements on the field based on color, or
   determining if a game element belongs to your alliance.

AprilTag Advantages
~~~~~~~~~~~~~~~~~~~

-  Very efficient with a fast detection rate (estimated 15 to 20
   detections per second, depending on decimation and target size).
-  Provides accurate, relative pose information of camera to target 
   in field coordinates.
-  Is less prone to fluctuating or varied lighting conditions on 
   the field.

.. figure:: images/AprilTagTelemetry.jpg
   :align: center
   :width: 25%

   AprilTag can provide accurate pose information to target


AprilTag Disadvantages
~~~~~~~~~~~~~~~~~~~~~~

-  The entire AprilTag must be in the camera view in order to be 
   recognized, any occlusions render the object unprocessable.
-  AprilTags must be included in the tag library in order to 
   process pose information for the tag (tag size and value must
   be known to the AprilTag system in advance).
-  Cameras require calibration data for every resolution used 
   in order to process correct pose information.

.. figure:: images/AprilTagDual.png
   :align: center
   :width: 75%

   AprilTags not in Tag Library detected, but no pose data available

