# MxGraphDiagram widget for Thingworx

View diagrams generated with [draw.io](https://draw.io), interact with them and more. It uses the [mxGraph](https://jgraph.github.io/mxgraph/) library.

# About
This is a Thingworx widget allowing visualization of dynamic [draw.io](https://draw.io) diagrams. The diagrams themselves can be exported from draw.io, or, generated dynamically by a service.

# Usage

The main entry point for the widget is the `XMLDiagram` property. This represents a mxGraph XML model.

###  3. <a name='Bindingsandproperties'></a>Bindings and properties

* `XMLDiagram`: An mxGraph xml containing the diagram. Can be either copied over from draw.io _Extras->Edit Diagram_ menu, or generated using a service.
* `ShowTools,ShowOutline`: Show or hide the helper windows allowing zooming into the diagram, printing it, and more.
* `AutoFit`: Make the graph fit the container when it first loads.
* `CustomShapesXMLPath`: URL that points to a xml shapes file that will be loaded at stratup.
* `EditedCellId`: The id of the cell where the label just changed. Tied to the CellLabelChanged event.
* `EditedCellNewLabel`: The contents of the cell where the label just changed. Tied to the CellLabelChanged event'. 
* `JSONArrayGraphCells`: Override allowing you to do state formatting on the element. It should be an JSON object containing id, value, fillColor and strokeColor.
* `SelectedCellId`: The Id of the currently selected cell.
* `AutoLayout`: The layout algorithm to be applied in the cells in the diagram. By default, no algorithm is selected, meaning that the positions of the cells in the XML are respected. If one algorithm is selected, the graph will be organized acording to that layout.
* `EdgeStyle`: Override the edge style algorithm in the XML. Usually used toghether with `AutoLayout`, allows for generation of good looking edged between cells.


The following events are also available:
* `CellLabelChanged`, `SelectedCellChanged`, `CellDoubleClicked`.


###  4. <a name='Installation'></a>Installation
- Navigate to the [releases page](/releases)
- Under the latest release, view all the assets
- Download the file `mxdiagram-min-<VERSION>.zip`
- Import the widget into Thingworx

# Development
This projects welcomes contributions. For details about pre-requisites, development environment and file structure, please see stefan-lacatus/ThingworxDemoWebpackWidget. 

##  1. <a name='Build'></a>Build

The following commands allow you to build and compile your widget:

* `npm run build`: builds the extension. Creates a new extension zip file under the `zip` folder.
* `npm run watch`: watches the source files, and whenever they change, do a build
* `npm run upload`: creates a build, and uploads the extension zip to the thingworx server configured in `package.json`.

#  Resources


#  Gallery

![mxGraph](demo/img/mxGraph1.png)

![mxGraph](demo/img/mxGraph2.png)

![mxGraph](demo/img/mxGraph3.png)

# Author
Petrisor Lacatus  (@stefan-lacatus) - IOT Presales Engineer, Romania CoE Team



# Disclaimer
By downloading this software, the user acknowledges that it is unsupported, not reviewed for security purposes, and that the user assumes all risk for running it.

Users accept all risk whatsoever regarding the security of the code they download.

This software is not an official PTC product and is not officially supported by PTC.

PTC is not responsible for any maintenance for this software.

PTC will not accept technical support cases logged related to this Software.

This source code is offered freely and AS IS without any warranty.

The author of this code cannot be held accountable for the well-functioning of it.

The author shared the code that worked at a specific moment in time using specific versions of PTC products at that time, without the intention to make the code compliant with past, current or future versions of those PTC products.

The author has not committed to maintain this code and he may not be bound to maintain or fix it.


# License
I accept the MIT License (https://opensource.org/licenses/MIT) and agree that any software downloaded/utilized will be in compliance with that Agreement. However, despite anything to the contrary in the License Agreement, I agree as follows:

I acknowledge that I am not entitled to support assistance with respect to the software, and PTC will have no obligation to maintain the software or provide bug fixes or security patches or new releases.

The software is provided “As Is” and with no warranty, indemnitees or guarantees whatsoever, and PTC will have no liability whatsoever with respect to the software, including with respect to any intellectual property infringement claims or security incidents or data loss.
