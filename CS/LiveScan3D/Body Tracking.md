---
onenote-id: 0-eb4a284aec2706891edaaab9088380d2!1-D084F068F621FF9!3717
---
[Vanogos Pterneas - Azure Kinect: Color + Depth + Body Tracking (C#/C++)](https://pterneas.com/2020/03/19/azure-kinect/)
 
[Kinect V2 Docs](https://docs.microsoft.com/en-us/previous-versions/windows/kinect/dn799271\(v=ieb.10\))
 
[Azure Documentation](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master)  
[Body Tracking Documentation](https://microsoft.github.io/Azure-Kinect-Body-Tracking/release/1.x.x/index.html)
 
[Washington - Kinect v2 SDK C++ - 4. Kinect Body Tracking](https://homes.cs.washington.edu/~edzhang/tutorials/kinect2/kinect4.html)

- LiveScanClient::UpdateFrame()
	- bool bNewFrameAcquired = pCapture-\>AcquireFrame();
	- pCapture-\>MapColorFrameToCameraSpace(m_pCameraSpaceCoordinates);
	- StoreFrame(m_pCameraSpaceCoordinates, pCapture-\>pColorRGBX, pCapture-\>vBodies, pCapture-\>pBodyIndex);
		- uint32_t tsCreation = 0;
		- CreateFramesReadyForTransmission(goodVerticesShort, goodColorPoints, tempBodies, finalVec, tsCreation);
		- m_clBuffer-\>Enqueue(finalVec, tsCreation, m_offsetUtcClock);

Each body frame contains three key components: a collection of body structs, a 2D body index map, and the input capture.
 \> From \<[https://docs.microsoft.com/en-us/azure/kinect-dk/build-first-body-app](https://docs.microsoft.com/en-us/azure/kinect-dk/build-first-body-app)\>  

[k4a_calibration_3d_to_2d](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/group___functions_ga2ed8b51d727425caa942aab190fc2ba9.html#ga2ed8b51d727425caa942aab190fc2ba9) (const [k4a_calibration_t](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/structk4a__calibration__t.html) *calibration, const [k4a_float3_t](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/unionk4a__float3__t.html) *source_point3d_mm, const [k4a_calibration_type_t](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/group___enumerations_ga8d5fae13125f360be86c166684cdb5c5.html#ga8d5fae13125f360be86c166684cdb5c5) source_camera, const [k4a_calibration_type_t](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/group___enumerations_ga8d5fae13125f360be86c166684cdb5c5.html#ga8d5fae13125f360be86c166684cdb5c5) target_camera, [k4a_float2_t](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/unionk4a__float2__t.html) *target_point2d, int *valid)
 \> From \<[https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/structk4a__calibration__t.html](https://microsoft.github.io/Azure-Kinect-Sensor-SDK/master/structk4a__calibration__t.html)\>  

# Body Index

576 x 640  
576 x 640 = 368,640 size
 
# Vertices to Process

576 x 1024 = 589,824 size  
589824/1024=576

- Not at full 4K resolution  
- AcquireFrame
- MapColorFrameToCameraSpace
	- UpdateDepthPointCloudForColorFrame
- StoreFrame
	- _Need mask here_

![ForC010rFrame 3731 depth 576x64 bodyindex 576x64 i...](../../img/OneNote/Body%20Tracking%20image%20d26bf2922f887b2c.png) ![3731depth 576x64 bodyindex 576x64 3741 depth 576x1...](../../img/OneNote/Body%20Tracking%20image%2092c7feef49d3642c.png) ![I info azureKinectCapture. cpp AzureKinectCapture ...](../../img/OneNote/Body%20Tracking%20image%20e6f7917f85dd43fd.png) ![unsigned _int64 _ Pos Line 1500 vertices, RG8 colo...](../../img/OneNote/Body%20Tracking%20image%20f2b9c8507fb60d34.png)