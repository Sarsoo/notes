---
onenote-id: 0-ab5da9885a9f0b611a7941d6671d96a8!1-D084F068F621FF9!3714
---

   
![FF](../../../../img/OneNote/Interpreting%20image%20368853562e8df9db.png)  

![Hartebeest Measuring Cup Ant Anemone Fish Banana P...](../../../../img/OneNote/Interpreting%20image%20a1f79944cbcc4e15.png) ![Exported image](../../../../img/OneNote/Interpreting%20image%20fee332ffba72cf3d.png)

# Maximising not SoftMax
 
- SoftMax normalisation will prefer images that ‘take away’ from p(interest) rather than contribute
	- Less clear visualizations (= so use final fc layer not SoftMax)
 ![Neuron Channel Class Logits LayerDeepDream Class P...](../../../../img/OneNote/Interpreting%20image%20b12b4138d13b8fa4.png)  

Grad-CAM  
Gradient weighted Class Activation Mapping
 
- Heatmap image for areas of focus
 ![VGG logitscat Source Image Act. Max. GradCAM VGG l...](../../../../img/OneNote/Interpreting%20image%203fb8d9a0a793ea93.png)  

- Use gradients going into last conv layer

![Exported image](../../../../img/OneNote/Interpreting%20image%20eb6206bf673505b8.png)  
![Logits output at fc layer prior to SoftMax for cla...](../../../../img/OneNote/Interpreting%20image%20634fb76baa34f616.png)  

![1 Get per channel for the class of interest global...](../../../../img/OneNote/Interpreting%20image%20966b6737bf82cc9b.png)

Adversarial Images
 
- Iteratively modify pixels to push CNN over decision boundary
 ![pdog 0.40 pcat 0.18 pplane 0.99](../../../../img/OneNote/Interpreting%20image%20276485373e666b21.png)  

# Fast Gradient

- Similar to activation maximisation
	- Set GT to class you want to shift it towards
 ![iteration 0 Image tending toward new class iterati...](../../../../img/OneNote/Interpreting%20image%2071828c249816c6e0.png)  

|   |   |
|---|---|
|![Targeted attack](../../../../img/OneNote/Interpreting%20image%2082a810be859c801d.png)|![Nin Untargeted attack](../../../../img/OneNote/Interpreting%20image%20c9522fbe0aaf3401.png)|

- Targeted
	- Misclassify as another class
- Untargeted
	- Just misclassify

![0.00 0 laundrydetergent3 vise 29003 50 1m 150 200 ...](../../../../img/OneNote/Interpreting%20image%201792f1740df0e172.png)