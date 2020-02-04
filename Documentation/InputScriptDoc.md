Lodis Perkins

s188043

Complex Game Systems

Modular Complex System Brief

# I. Requirements

## Description of Problem

### Name: Button Input Script

### Purpose:

The purpose of this script is to create an easier way to bind user defined functions to unity their corresponding input axis.

### Format:

The exstension consists of two c# scripts for unity.

# II. Getting Started

First, start by adding the InputVariable script and the InputButtonBehaviour script in the assets folder of your unity project.

![FileLocation](FileLocation.png)

Next, setup your input axis in the Unity input editor.

![InputAxis](Axis.png)

Now that the input axis has been set up, add the InputButtonBehaviour script to your gameobject.

![InputComponent](InputComponent.png)

- Inputs - The list of inputs the gameobject  has. Click on one of the inputs in this list to view it properties.
- Input Buffer- The amount of time needed to past before this inputs actions can be performed again.
- Input Axis Name - The name of the input axis in Unity's input editor.
- Button Down Func - The name of the function that will be called on the gameobject when the button is pressed.
- Button Up Func - The name of the function that will be called on the gameobject when the button is not pressed.
- Button Negative Func - The name of the function that will be called on the gameobject when the neagtive axis for this button has been pressed.
- Argument - The argument needed for the function being called when the button is pressed.
- Requires multiple inputs- Check this box if the input your adding needs multiple buttons to be pressed in order to call its function.
- Add Input - Click this to add an input to the list.
- Clear - Clears all inputs from the list.

# II. Design

## Object Information

### File Name: InputVariable.cs

Name: arg(object)

Description: the optional argument for this inputs function

Visibility: public

Name: buttonDownMessage(string)

Description: The name of the function to be called when this button is pressed

Visibility: public

Name: ButtonUpMessage(string)

Description: The name of the function to be called when this button is not pressed

Visibility: public

Name: ButtonNegativeMessage(string)

Description: The name of the function to be called when this button is pressed on the negative side of the axis

Visibility: public

Name: Axis(string)

Description: the name of the axis this input is responsible for

Visibility: public

Name: AxisNames(List<string>)

Description: List of axis names if this input requires multiple buttons

Visibility: public

Name: InputBuffer(string)

Description: The amount of time needed to perform a button down action

Visibility: public

Name: CheckTime()(bool)

Description: Checks to see if the enough time has passed since the last input

Visibility: public

Arguments: none

Name: init()(void)

Description: The initializer for this input

Visibility: public

Arguments: string axisName, string funcMessage1, string funcMessage2, string funcMessage3,object funcArg,float timer,bool hasMultiInput,List<string>buttons

Name: CreateInstance()(InputVariable)

Description: creates an instance of an input variable

Visibility: public

Arguments: string axisName, string funcMessage1,string funcMessage2, string funcMessage3, object funcArg, float timer, bool hasMultiInput, List<string>buttons

### File Name: InputButtonBehaviour.cs

Name: inputs

Description: The list of inputs the player has

Visibility: private

Name: newInput(inputVariable)

Description: Reference to the last input added

Visibility: private

Name: CheckButton()(Void)

Description: Checks the list to see if any of the button are down

Visibility: public

Name: CheckButtons()(Void)

Description: Checks the list to see if all of the required buttons are down

Visibility: public

Name: CheckInputs()(void)

Description: Calls the check input functions for each input

Visibility: public

