# Introduction #

The dynamic pipeline project is a graph-based approach towards extensible pipelines. It allows you to compose pipelines on-the-fly, depending on the required functionality. In this way, you don't need to create one specific pipeline for each task that you want to execute. To use the dynamic pipeline system you need only to download the project package and instantiate the Tool Registry with your own tools.

This project is suitable for pipeline applications with multiple functionalities that require different combinations of steps in each execution.

Our approach consists in representing the connectivity of pipeline components (programs or scripts) with a directed graph in which components are the graph edges, their inputs and outputs are the graph vertexes, and paths through the graph are pipelines with specific functionalities.

# Implementation #

The complete package consists of:

  * A tool registry. Data structure for storing information about all tools available in the system.
  * The dynamic pipeline java executable (`SetPipeline.class`). Creates pipelines on-the-fly based on the tool registry and start and end points.
  * The available pipelines java executable (`AvailablePipelines.class`). Finds all possible outputs that can be reached from a particular input through available pipelines.
  * The calculate performance java executable (`CalculatePerformance.class`). Calculates a performance measure for tools in the pipeline system.
  * The graph inspector java executable (`GraphInspector.class`). It provides information about the graph that is created from your tool registry file, such as the indegree and outdegree of the graph nodes.
  * Sample interface program written in PHP (`index.php`). It creates a web interface for
a dynamic pipeline system.

## Current Limitations ##

  * The package cannot yet be used for designing pipelines that require the execution of parallel steps, since it focus on the problem of finding alternative sequential steps to achieve a particular aim.
  * The system does not support the inclusion of tools with command lines requiring specific parameter definitions. Currently, pipelines are created with a composition of tools with a standard command line interface that allows for the specification of only one or more input files and one or more output files.

## Publication ##

Please cite us:

Rodrigues, M. R., Magalhaes, W. C. S., Machado, M., Tarazona-Santos, E. A Graph-based Approach for Designing Extensible Pipelines. **BMC Bioinformatics**, 2012, 13:163.

## Applications ##

<a href='Hidden comment: 
We successfully used the dynamic pipeline code to implement [http://pggenetica.icb.ufmg.br/divergenome/application/dynamicpipeline/tools.php a format conversion application].
'></a>

We successfully used the dynamic pipeline code to implement [DIVERGENOMEtools](http://pggenetica.icb.ufmg.br/divergenome/pagina/dynamicpipeline/tools.php), a format conversion application for popular software and data formats in population genetics and genetic epidemiology.

