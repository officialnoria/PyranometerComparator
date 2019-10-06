# Pyranometer Comparator

Source code is property of Centro Nacional de Metrologia, which I'm not authorized to show here, only still images.

This software was developed in National Instruments LabWindows/CVI as part of a joint project with the Autonomous University of Mexico City. As the title says, it is a pyranometer comparator between a calibrated pyranometer and a device under test (DUT). The software acts as a sequence generator, since the tests are not always the same, or require the same instruments.

When the user opens the software, all functionality is immediately available, as shown in the image below:

![Main window](/Main.jpg)

If the user has a predefined sequence stored on memory, the button CARGAR SECUENCIA allows the user to locate the file and open it. Doing so will populate the textbox with the sequence information, such as number of measurements and extra parameters. But if the user does not have a sequence stored in memory, the button OPERACIONES E INSTRUMENTOS opens the following window:

![Instruments window](/Instruments.jpg)

In this window, the user can choose for each of the instruments, what actions must the software perform when the test begins. For example, setting the power source's output voltage or the number of measurements to be made with the datalogger.

This window also has two arrow buttons that rotate a small table via a stepper motor. In this table the calibrated pyranometer and the DUT are fixed. The arrow buttons allow the user to ensure horizontality in one axis (normally it's for the calibrated pyranometer), then the table is rotated 180 degrees, and the DUT is aligned manually.

The user can also set a pause time between two operations, completely pause the software at some point or add a comment to an operation.

Once the full sequence has been created, the user can save it to memory via the GRABAR SECUENCIA button. The button PUERTOS COM in the main window, when clicked, opens a COM port selector for each instrument, it usually does not change in the same computer, but it does change if the software is used in other computer.

Finally, the button EJECUTAR SECUENCIA executes the sequence in the order the user specified it, when clicked it allows the user to enter the number of repetitions the sequence executes (the user must ensure circularity of the sequence), the user can stop the execution at any moment. At each point of the execution, it saves information in a txt file for further analysis.
