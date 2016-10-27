# BPMN2Requirements
Model-based architecture for the generation of textual requirements from business processes defined with BPMN.

This repository is structured as follows:

- Article/ It contains an article, written in spanish, describing the architecture. The article was accepted and presented in the spanish conference "XX Jornadas de Ingeniería del Software y Bases de Datos (JISBD 2015)".

- BMPN2toRequirements/ It contains the actual project, structured as follows:
	- metamodels/ It contains the BPMN2 metamodels and our own TaskBusiness metamodel.
	- models/ It contains the BPMN2 models from which the textual requirements are generated. It currently contains some example BPMN models.
	- output/ It contains the generated text files with the textual requirements corresponding to every BPMN model. It currently contains the textual requirements generated for the example BPMN models.
	- transformations/ It contains the model to model (m2m) and model to text (m2t) transformations that are necessary to generate the requirements. The transformations have been defined using the Epsilon[1] framework.
	- launch.xml An ANT script to launch the process.


The execution process is as follows:

1. The BPMN models are placed in the models folder. There is currently no support for importing BPMN diagrams in other formats. Instead, models conforming the BPMN2 metamodel must be provided. These models can be easily defined using the Eclipse BPMN2 Modeler[2].
2. The process is launched using the launch.xml ANT script. The script contains the necessary instructions.
3. The textual requirements are generated in the output folder.


[1] Epsilon. http://eclipse.org/epsilon/
[2] BPMN2 Modeler. http://www.eclipse.org/bpmn2-modeler/