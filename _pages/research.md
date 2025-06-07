---
layout: page
permalink: /research/
title: Research
#description: Materials for courses you taught. Replace this text with your description.
nav: true
nav_order: 4
---




#### 1. Artificial muscle

We focus on not only design novel and useful artificial muscles, but also study the modeling, control, and implementation of them into robots. 

--------------------

##### Fiber-reinforced pneumatic twisted-and-coiled actuator (FR-PTCA)
<div style="display: flex; align-items: top;">
  <div style="flex: 1; padding-right: 30px;">
    <p style="text-align: justify;">
        The fiber-reinforced pneumatic twisted-and-coiled actuator (FR-PTCA) is a novel soft actuator that overcomes key limitations of existing designs such as the Cavatappi muscle. By incorporating a fiber reinforcement to enhance tube anisotropy, the FR-PTCA achieves significantly improved performance. It delivers higher energy efficiency (over 19%), lower required input pressures (130 psi), and maintains a large contraction strain (up to 70%). In contrast, the Cavatappi muscle, while offering desirable attributes such as compliance, low cost, and large linear contraction with minimal radial expansion, suffers from low energy efficiency (~9%) and demands high-pressure inputs (over 240 psi).
    </p>

  </div>

  <div style="flex: 1;">
    {% include youtube.html id="fIU39fBoaMc" max_width="425px" title="Sp2025 final project" %}
  </div>
</div>


 Publication:
1. E. Weissman, B. Ashcroft, P. Nguyen, and J. Sun, “Efficient Pneumatic Twisted-and-Coiled Actuators Through Dual Enforced Anisotropy,” IEEE/ASME Transactions on Mechatronics, pp. 1–9, 2025


------------------------

##### Twisted-and-coiled actuator (TCA) 

<div style="display: flex; align-items: top;">
  <div style="flex: 1; padding-right: 30px;">
    <p style="text-align: justify;">
        Twisted and Coiled Actuators (TCA) are lightweight, low-cost artificial muscles made by twisting and coiling polymer fibers. When electrically heated, they contract along their length, mimicking natural muscle motion. Their high power-to-weight ratio and flexibility make them ideal for soft robotics.

        My research focuses on designing free-stroke TCAs that achieve large, untethered contractions and incorporate self-sensing for closed-loop control without external sensors. I apply these actuators in diverse robotic systems, including soft robotic arms, bistable jumping robots, and morphing structures. Additionally, I develop models to capture the mechanical and thermal behavior of TCAs and TCA-driven robots, enabling precise control and adaptive functionality in soft robotic applications.
    </p>

  </div>

  <div style="flex: 1;">
    {% include figure.html path="assets/img/research/TCA_reserach.jpg" title="Open Door 2025" class="img-fluid rounded z-depth-1" width="500" %}
  </div>
</div>


Publication:
1.  J. Sun, E. Lerner, B. Tighe, C. Middlemist, and J. Zhao, “Embedded shape morphing for morphologically adaptive robots,” Nature Communications, vol. 14, no. 1, p. 6023, Sep. 2023
2. J. Sun, B. Tighe, Y. Liu, and J. Zhao, “Twisted-and-coiled actuators with free strokes enable soft robots with programmable motions,” Soft robotics, vol. 8, no. 2, pp. 213–225, 2021
3. J. Sun, B. Tighe, and J. Zhao, “Tuning the Energy Landscape of Soft Robots for Fast and Strong Motion,” in 2020 IEEE International Conference on Robotics and Automation (ICRA), May 2020, pp. 10 082–10 088
4. J. Sun and J. Zhao, “Integrated actuation and self-sensing for twisted-and-coiled actuators with applications to innervated soft robots,” in 2020 IEEE/RSJ International Conference on
Intelligent Robots and Systems (IROS). IEEE, 2020, pp. 8795–8800


------------------------------


#### 2. Wearable robotics

##### Back-support device

<div style="display: flex; align-items: top;">
  <div style="flex: 1; padding-right: 30px;">
    <p style="text-align: justify;">
        Back support devices (BSDs) have the potential to mitigate overexertion in industrial tasks and also to provide assistance to people with weak back muscle strength in daily activity. While state-of-the-art active BSDs can offer a high assistive force, they are bulky and heavy, making them uncomfortable for daily use. On the contrary, passive BSDs are compact but need manual adjustment to be versatile. This work presents a hybrid soft BSD that can provide task-oriented assistance by tuning the stiffness (0.58 N/mm, 0.92 N/mm, and 1.7 N/mm) and slack length (0 mm to 67 mm) in a compact design. The tunable stiffness allows for selecting a task-specific force profile, and the slack tuning will ensure that the device enables unhindered movement when assistance is not required.
    </p>

  </div>

  <div style="flex: 1;">
    {% include figure.html path="assets/img/research/backsuit.png" title="Open Door 2025" class="img-fluid rounded z-depth-1" width="480" %}
  </div>
</div>


Publication:
1.  R. Khatavkar, T. B. Nguyen, Y. Chen, H. Lee, and J. Sun, “A Hybrid Variable-Stiffness Soft Back Support Device,” IEEE Robotics and Automation Letters, vol. 10, no. 4, pp. 3238–3245,
Apr. 2025
    

#### 3. Modeling and Control of soft robots

------------------------

##### Koopman based continuum robot control

<div style="display: flex; align-items: top;">
  <div style="flex: 1; padding-right: 30px;">
    <p style="text-align: justify;">
     We work on Koopman-based modeling and control introduces a physics-informed, data-driven framework for managing the complex, nonlinear dynamics of soft robots. By employing the Koopman operator theory, he transforms the nonlinear behavior of soft continuum manipulators into a higher-dimensional but approximately linear representation. This enables the use of efficient linear control techniques, such as convex optimization, for real-time shape control. His approach enhances computational efficiency while preserving the expressiveness needed to model soft robotic deformations, bridging the gap between accurate modeling and practical, fast control strategies.
    </p>

  </div>

  <div style="flex: 1;">
    {% include figure.html path="assets/img/ristich_icra_2025/flow_chart.png" title="Physics based Koopman" class="img-fluid rounded z-depth-1" width="250" %}
  </div>
</div>

Publication:
1. E. Ristich, L. Zhang, Y. Ren, and J. Sun, “Physics-informed Split Koopman Operators for Data-efficient Soft Robotic Simulation,” in 2025 International Conference on Robotics and Automation (ICRA). IEEE, 2025 (Accepted) 
2. A. Singh, J. Sun, and J. Zhao, “Controlling the Shape of Soft Robots Using the Koopman
Operator,” in 2023 American Control Conference (ACC), May 2023, pp. 153–158

------------------------------

##### Physics-based modeling 

<div style="display: flex; align-items: top;">
  <div style="flex: 1; padding-right: 30px;">
    <p style="text-align: justify;">
        Physics-based modeling in soft robotics centers on developing analytical frameworks that accurately capture the behavior of soft robots actuated by Twisted-and-Coiled Actuators (TCAs). Leveraging Cosserat rod theory, his models incorporate the nonlinear, coupled interactions between soft structures and multiple TCAs routed in complex geometries. This enables the prediction and control of soft robot motions—such as bending, twisting, and grasping—with high fidelity. His modeling approach balances mechanical realism with computational efficiency, providing a foundational toolset for design, simulation, and control of multifunctional soft robotic systems.
    </p>

  </div>

  <div style="flex: 1;">
    {% include figure.html path="assets/img/research/physics-based_modeling.png" title="physics based modeling" class="img-fluid rounded z-depth-1" width="550" %}
  </div>
</div>

Publication:
1.  J. Sun and J. Zhao, “Physics-based modeling of twisted-and-coiled actuators using  cosserat rod theory,” IEEE Transactions on Robotics, vol. 38, no. 2, pp. 779–796, 2022.
2.  J. Sun and J. Zhao, “Modeling and Simulation of Soft Robots Driven by Embedded Artifi- cial Muscles: An Example using Twisted-and-Coiled Actuators,” in 2022 American Control Conference (ACC). Atlanta, GA, USA: IEEE, Jun. 2022, pp. 2911–2916


------------------------------

