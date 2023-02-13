# Choosing an Actuator

Choosing between actuators can be a difficult process. Without applying physics and math, you may be left wondering how to make the choice between an HD Hex Motor (

[REV-41-1301](https://www.revrobotics.com/rev-41-1301/)

) and a Core Hex Motor (

[REV-41-1300](https://www.revrobotics.com/rev-41-1300/)

)? This section will take you through the process and mathematics to help you make the best decision for your robot!

Before getting too far here are some general guidelines for where REV DUO actuators are best utilized.

|   |                                             |
| - | ------------------------------------------- |
|   | Drivetrains, Elevators, and Arms            |
|   | Lighter duty arms and intakes               |
|   | Lighter duty intakes, switches, and latches |

Though these basic suggestions are here to guide you in the right direction, all robots are different. Follow through the rest of this guide to find the best fit for your mechanisms.

When designing a robot, selecting the correct actuator for the application is a critical design challenge. Some tools can be used to estimate the performance of a motor in a particular application.

Understanding these basic concepts is required to make optimized design decisions which consider the trade-offs inherent to any design. This section will briefly cover the definition of these concepts and then explain them in relationship to basic powertrain concepts.

_**Speed**_ is the measure of how fast an object is moving. The **speed** of an object is how far it will travel in a given amount of time. For rotating parts like gears and wheels, **speed** is expressed in how many revolutions are made in a given amount of time. Under ideal conditions, the rotation of a wheel is converted into linear **speed** and can be calculated by multiplying the diameter of the wheel by the rotations for a given time. The SI unit for **speed** is meters per second, but **speed** is also commonly expressed in feet per second.

_**Angular Velocity**_ is how the speed of a rotating object is described. The SI unit for the _**Angular Velocity**_ is radians per second (rad/s), revolutions per minute is also commonly used.

_**Torque**_ is roughly the measure of the turning force on an object like a gear or a wheel. Mathematically, **torque** is defined as the rate of change of the angular momentum of an object. This can also be stated as a force that acts normal (at 90 degrees) to a radial lever arm which causes the object to rotate. A common example of torque is the use of a wrench in order to tighten or loosen a bolt. In that example, using a longer wrench can produce more **torque** on the bolt than using a shorter wrench. **Torque** is commonly expressed in N⋅m or in⋅lbs.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F15mm%2F-M8MarlMx5meMXBAcMX\_%2F-M8MhYlOGaVPJjMAAlCw%2F3.png?generation=1590609462353188\&alt=media)

When **torque** is turning an object like a spur gear, the gear will create a straight line (linear) force at the point where the teeth contact the other gear. The magnitude of the **torque** created is the product of the rotational force applied and the length of the lever arm which in the case of a gear, is half of the pitch diameter (the radius).

_**Work**_ is concept used to describe changes in energy. Path independent _**work**_ is defined as force times displacement; for example if a 1 kilogram(kg) weight is lifted vertically 1 meter(m) against gravity at a constant velocity the work done is:

​

1(kg)∗9.8(m/s2)∗1(m)=9.8(kg∗m2/s2)1(kg)\*9.8(m/s^2)\*1(m) = 9.8 (kg\*m^2/s^2)

or 9.8 joules(J).

_**Power (P)**_ is the rate of work over time. The concept of **power** includes both a physical change and a time period in which the change occurs. This is different from the concept of work which only measures a physical change. The difference in these two concepts is that it takes the same amount of work to carry a brick up a mountain whether you walk or run but running takes more **power** because the work is done in a shorter amount of time. The SI unit for **power** is the Watt (W) which is equivalent to one joule per second (J/s). Rotational **power** is calculated by multiplying **torque** and **angular velocity**.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F15mm%2F-M8MarlMx5meMXBAcMX\_%2F-M8MhYlPE4LA1JOHrdyQ%2F4.png?generation=1590609462303710\&alt=media)

In competitive robotics, the total amount of available power is determined by the motors and batteries allowed. The maximum speed at which an arm can lift a certain load is dictated by the maximum system **power**.

### Choosing an Actuator Walkthrough <a href="#choosing-an-actuator-walkthrough" id="choosing-an-actuator-walkthrough"></a>

_This section will utilize key metrics and terms from the_

_Motor_

_and_

_Servo_

_pages. Please visit those pages before going through this walk-through._

The first round of analysis to narrow down your actuator is to compare the the maximum output power of the actuator to the power required to run the mechanism.

Lets say you are building an elevator that lifts a game piece. Before you can begin your calculations you have to make some basic assumptions about your design. In this case, assume zero frictional losses and instantaneous acceleration. Consider also, the following information:

* Game piece weight: 0.5 kg
* Lifter maximum height: 1.5 meters
* Time to full extension: 5 seconds

For extra practice try running the same calculations but with t = 10 seconds instead of t = 5 seconds.

**Work** is a concept used to describe changes in energy. Path Independent **work** is defined as force times displacement. Since Force is mass times acceleration the following formula for work can be derived:

As a standard when calculating work, calculate **Net Work,** or the total amount of forces displacing your mechanism. In the example, the only force to account for is the acceleration against gravity at a constant velocity, as it has been assumed there are no frictional forces at play. Therefore in the example Work is:

2(kg)∗9.8(m/s2)∗1.5(m)=29.4joules(j) 2(kg) \* 9.8(m/s^2) \*1.5(m) = 29.4 joules(j)

Where the 2(kg) = the combined mass of the elevator and the game element.

The example given is a simplified version assuming that no other forces are at play. For optimal results take time to consider what forces may affect the work done by your mechanism.

#### Step 2: Calculating Power <a href="#step-2-calculating-power" id="step-2-calculating-power"></a>

**Power (P)** is the rate of work over time. The difference between work and power is that it takes the same amount of work to carry a brick up a mountain whether you walk or run, but running takes more power because the work is done in done in a shorter amount of time. So, power can be represented as:

P=W/tP = W/t

,where t = time period

In the example, work was calculated to be 29.4. It was also stated that the time period is 5 seconds. With those numbers known power can be calculated as:

29.4J/5s=5.88Watts29.4 J / 5s = 5.88 Watts

What is power if the elevator reached full height in 10 seconds rather than 5?

When you are building a mechanism it is advisable to apply a **safety factor (sf)** to the power of the mechanism to ensure that your mechanism is able to withstand things like unexpected loads or degradation over time. For this example, apply a safety factor of 2.

Remember these calculations are made with an assumption of no friction. The safety factor helps to account for some of the assumptions made with this example.

5.88W∗2sf=12watts5.88W \* 2 sf = 12 watts

After applying the safety factor of 2 and rounding, it is found that 12 watts of power are needed to power the mechanism. Now that the power estimate is known it is time to decide which actuator meets the criteria given.

What do you get for the t = 10 seconds calculation if sf = 2?

#### Step 3: Choosing an Actuator <a href="#step-3-choosing-an-actuator" id="step-3-choosing-an-actuator"></a>

Take the known power estimate of 12 watts and compare it against the **Maximum Output Power** for the various actuators in the key metric table. Choose a motor that has a maximum output power greater than that of the estimated power for the mechanism. With those parameters given, the likely choices for the elevator are any of the HD Hex Motor variants.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-M8WcLi6koTauMV2xJ63%2F-M8Wcn1G5NwpGNhgHWaD%2FScreenshot%20\(20\).png?alt=media\&token=e1ac32df-44fb-4452-a956-aa09ee5a2b45)

What actuator would you choose for the same mechanism if the amount of power you need is 6W?

#### Step 4: Estimating Performance <a href="#step-4-estimating-performance" id="step-4-estimating-performance"></a>

A motor performance graph can be used both for selecting a motor and for understanding the motors behavior once installed in the robot. The below prototypical performance graph can be used to estimate the performance of a motor.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-M8pWUYkwh9D9UsG91zc%2F-M8phcq0tDwLkq6LQav6%2Fimage.png?alt=media\&token=a880b47e-10e2-4dbb-aafd-ea7b0f716ff5)

The prototypical performance graph exhibits standard curves to help calculate where your motor falls on the performance scale.

**Using the Performance Curve to Select an Actuator**

When selecting a motor the expected power requirement for the motor is used. In the example estimate power was found to be 12 watts. The graphic below for finding power/torque range has a power estimate similar to that of the example (12 watts is 80% of max power). This will still be a good example of how to use the motor performance graph to estimate your metrics.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-M8pWUYkwh9D9UsG91zc%2F-M8psYWV\_Hvt6cdiTU8y%2Fimage.png?alt=media\&token=fdb2fcdf-4820-443f-806b-cf4ccf609db2)

**Using the Performance Curve to Understand Behavior**

If you have already selected an actuator and installed it you may want to check to see what your robots performance is. This process is similar to the estimation to select a motor.

Previously the power estimate was used to find the other metrics, now amperage will be used as it can be reported by the Control Hub (

[REV-31-1595](https://www.revrobotics.com/rev-31-1595/)

) and Expansion Hub (

[REV-31-1153](https://www.revrobotics.com/rev-31-1153/)

). When amperage is known, draw a line horizontally at the known value using the current scale, then at the point your horizontal line intersects the current curve, draw a vertical line. The points at which the vertical line intersects the key metric curves will give you the estimated performance for each metric.

When designing with **minimal constraints it is best maximize power and efficiency**. The point of maximum efficiency usually occurs around the 25% of maximum torque point.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-M8pWUYkwh9D9UsG91zc%2F-M8ptKXvYNf3lT5LlIjF%2Fimage.png?alt=media\&token=177f6746-9d44-43ca-9f8a-6ffa02c7f851)

#### Step 5: Powertrain Design <a href="#step-5-powertrain-design" id="step-5-powertrain-design"></a>

Once a motor has been selected, a power train can be designed. The goal of the power train is getting the final **torque** and **angular velocity** to the necessary values within the possible range that can be produced by the motor. When designing the power train, the fewer elements present in the power train the more efficient the power train will be. For example, using 30:72 gear box and a 20:20 chain drive will be less efficient than directly using 20:54 chain drive.

As a rule, gears are more efficient than chain drive.

Motor performance curves are useful at this stage of design as well because given an estimated power requirement you can estimate an angular velocity and torque range that the motor will be outputting. When designing the power train, the values used should be at the lower end of the viable rpm and torque range as the motor can be given more power to bring it into performance should the estimates be off.
