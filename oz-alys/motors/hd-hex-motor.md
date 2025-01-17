# HD Hex Motor

The HD Hex Motor (

[REV-41-1301](https://www.revrobotics.com/rev-41-1301/)

) features an integrated encoder and power that plug right into the REV Control Hub (

[REV-31-1595](https://www.revrobotics.com/rev-31-1595/)

) and Expansion Hub (

[REV-31-1153](https://www.revrobotics.com/rev-31-1153/)

). The gearbox options feature 5mm Hex output or coupler making it easy to connect gears, sprockets, wheels, etc. Encoder and power cables are always included with motor. The HD Hex Motor is similar in size and power to other brushed 550 class motors with more convenient output options and connectors.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-M95GzREAfvShYd-fr7k%2F-M95JnKjgsxv73CPT0aB%2FMini%20Chart%20HD%20Hex.png?alt=media\&token=58f8a82e-21a1-4539-87cf-f253e9357881)

The HD Hex Motor matches the design flexibility of other REV products with a series of compatible gearboxes to choose from. Gearbox options include the UltraPlanetary Gearbox (

[REV-41-1600](https://www.revrobotics.com/rev-41-1600/)

), Spur Gearboxes, Planetary Gearbox, and no gearbox.

This section will focus on general HD Hex Motor information such as motor specifications and mounting techniques.

_To learn more about gears and how they work with the HD Hex Motor visit the_

_gears_

_page._

The HD Hex Motor uses a 2-pin JST-VH Connector for motor power and a 4-pin JST-PH for sensor feedback from the built-in encoder. For more information on using the cables and connectors included with the HD Hex Motor, see the

[REV Control System - Cable and Connectors documentation](https://docs.revrobotics.com/duo-control/control-system-overview/cables-and-connectors)

. The image below has the pinout for the motor power and the encoder.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-M\_M8cPZpdT88Tye8xPn%2F-M\_MCcUszaBq8eeo9Rmp%2FHD%20Hex%20Motor\_Encoder%20Pinout1\_Export.svg?alt=media\&token=b7cf4b6d-d8aa-407c-bf6d-609253e815cf)

### HD Hex Motor (No Gearbox) <a href="#hd-hex-motor-no-gearbox" id="hd-hex-motor-no-gearbox"></a>

Why would you get a motor without a gearbox? Lets consider a few scenarios:

*   **​**

    [**Motors Can Fail**](broken-reference)

    \- If you have a motor that has failed but the gearbox is still in good condition, it is typically cheaper to buy the bare motor and attach the gearbox you already have.
*   **​**

    **Customization**

    \- If you want to make your own gearbox, having the No Gearbox version of the motor will make that easier.

If you are planning to make a custom gearbox keep in mind that the bare HD Hex motor comes pre-pressed with a pinion for the spur gearboxes.

* Encoder Counts per Revolution
  * At the motor - 28 counts/revolution

If you are creating a custom gearbox or using the UltraPlanetary Gearbox, the specifications for the bare motor will help you calculate key metrics for your actuator.

Planetary gearboxes are designed for increased robustness when compared to Spur gearboxes, and are generally less susceptible to damaging shock loads due to more gear teeth being engaged to carry the load. There are a two planetary gearbox options from REV, the 20:1 Planetary gearbox (

[REV-41-1211](https://www.revrobotics.com/rev-41-1301/)

) and the UltraPlanetary gearbox. The 20:1 Planetary gearbox has a set gear ratio where the UltraPlanetary allows for swapping out of cartridges to adjust the final gear ratio.

The UltraPlanetary System is a cartridge based modular gearbox designed to handle the rigors of the competition and the classroom. The UltraPlanetary System includes an input stage and pinion gear that works with the REV HD Hex Motor and other 550 class motors. Building on the ability to iterate and adjust designs easily using the REV Building System, the UltraPlanetary System consists of pre-assembled and lubricated cartridges allowing for swapping gear ratios on the fly and with ease. Users can configure a single-stage planetary using one of three different reduction cartridges, build multi-stage gearboxes through stacking individual cartridges together, and choose two different ways for transferring power: either through face mounting directly on the output stage or choosing the length of 5mm hex shaft best suited for the application.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-M95GzREAfvShYd-fr7k%2F-M95HrIOql0y5Mtpa\_5D%2Fimage.png?alt=media\&token=6bdf6103-ef95-4b6b-b73c-7f4165cf8e0d)

A wide range of gear ratios are possible with the three included cartridges. When combining up to three cartridges, just multiply each cartridge gear ratio to find the overall gear ratio. For example, a combination of the 4:1 and 5:1 cartridges would make a 20:1 overall gear ratio. The table below shows the common use cases for all possible ratios that can be created with the included UltraPlanetary kit.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-MJXX0TwZHCQtbo5jlvZ%2F-MJXXXABPEZRY9rex8B5%2FGear%20Ratio%20Table.png?alt=media\&token=5a3e4182-9680-486c-997c-4aa653d49817)

Below are the specifications for a small sample of the options available with the UltraPlanetary Gearbox Kit.

| Nominal Gear Ratio | Actual Gear Ratio | Free Speed | Stall Torque | Weight              |
| ------------------ | ----------------- | ---------- | ------------ | ------------------- |
| 5:1                | 5.23:1            | 1147 RPM   | 0.55 Nm      | 371 g (0.818 lbs)   |
| 20:1               | 18.9:1            | 317 RPM    | 1.98 Nm      | 405 g (0.893 lbs)   |
| 60:1               | 54.8:1            | 109.5 RPM  | 5.75 Nm      | 441.5 g (0.973 lbs) |

The 20:1 Planetary gearbox features mounting holes on a 14mm bolt circle. The gearbox is compatible with the Planetary Gearbox Flat and Bent motor mounting brackets. To mount the 20:1 Planetary directly to the Extended Motion Pattern on REV Channel use a HD Hex Planetary Facemount Spacer.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-MC8mVuJSPMzBDzoM-ex%2F-MC8mx1n0nJNcMAHrpn0%2FHD%20Hex%20Motor%20Planetary%20Documentation%20Graphic%20Motor%20Pinout%20GitBook%20Sized-01.png?alt=media\&token=5e6f6dea-afb8-4336-a0f2-2550a731344f)

* Weight: 436g (including motor)
* Output Shaft Length: 40mm
* Free Speed: 300 rpm (31.4 rad/s)
* Stall Torque: 297.4 oz-in (2.1 Nm)

The Spur gearboxes feature the REV Motion Pattern that is compatible with REV Motion Brackets and the Extended Motion Pattern on REV Channel. There is a second mounting pattern that is standard for most spur gearboxes. This pattern is featured on the flat and bent motor mounting brackets for Spur Gearboxes.

![](https://2589213514-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-M5yw0n8IneF5-9ybLjT%2F-MBu5Hagb9DD2a2TeOJQ%2F-MBu5lpsWhnIbueBwrjm%2FHD%20Hex%20Motor%20Spur%20Documentation%20Graphic%20Motor%20Pinout%20GitBook%20Sized-01.png?alt=media\&token=dea1f198-63f4-49e2-8a70-c7608f788e84)

* Weight: 350g (including motor)
* Output Shaft Length: 40mm
* Mounting Holes: 10 - M3 tapped - use a 5mm length or shorter bolt
* Free Speed: 300 rpm (31.4 rad/s)
* Stall Torque: 297.4 oz-in (2.1 Nm)
* Weight: 350g (including motor)
* Output Shaft Length: 40mm
* Mounting Holes: 10 - M3 tapped - use a 5mm length or shorter bolt
* Free Speed: 150 rpm (15.7 rad/s)
* Stall Torque: 594.7 oz-in (4.2 Nm)
