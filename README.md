# Introduction #

To run the dynamic pipeline project you need: (1) the dynamic pipeline directory structure provided as a .tar file, which includes the dynamic pipeline algorithm (`SetPipeline.class`), the available pipelines algorithm (`AvailablePipelines.class`) and the program to calculate the tools' performance measure (`CalculatePerformance.class`), all written in Java ; (2) a set of tools to be part of the pipeline system, stored in the folder "tools/"; and (3) the tool registry file (`registry/ToolRegistry.txt`) instantiated with information about the tools in "tools/". If you want to access your dynamic pipeline system through a web interface, we provide a sample interface program written in PHP (index.php). Requirements for using the dynamic pipeline project are below.

# Requirements for the Java Algorithm #

  * Library jgrapht-0.8.1  (provided along with the project files)

  * Directory hierarchy (creation required beforehand):

> dynamicpipeline/java/

> dynamicpipeline/java/jgrapht-0.8.1/

> dynamicpipeline/registry/

> dynamicpipeline/tools/

> All with read+exec permissions

  * Directory hierarchy (created on execution):
> dynamicpipeline/inputs/
> dynamicpipeline/pipelines/

> All with read+exec+write permissions

  * Complementary files:
> ToolRegistry.txt (on dynamicpipeline/registry/)

> With read+exec+write permission


**ATENTION:** before running the java programs you must
  1. populate the folder "tools/" with the tools you want to include in your pipeline system; and
  1. instantiate the Tool Registry (`registry/ToolRegistry.txt`) with information about those tools. Read the document on the Wiki section about how to incorporate your tools.