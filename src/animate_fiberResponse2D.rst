.. include:: sub.txt

=================================
 animate_fiberResponse2D command
=================================

.. function:: postprocessing.Get_Rendering.animate_fiberResponse2D(Model, LoadCase, element, section,
                                  LocalAxis='y', InputType='stress', skipStart=0, skipEnd=0, rFactor=1, 
								   outputFrames=0, fps=24, Xbound=[], Ybound=[])

   Animates fiber output distribution along the Y-axis of the fiber section.

   ========================  =========================================================================================================
   ``ModelName`` |str|        Name of the model to read data from output database, created with `createODB()` command.
   ``LoadCaseName`` |str|     Name of the subfolder with load case output data.
   ``element`` |int|          Tag of the element where the section to be plotted is located.
   ``section``  |int|         Tag of the section to be plotted.
   ``LocalAxis`` |str|        Local axis of the section, based on a user defined axes transformation. (optional, default is "Y")
   ``InputType`` |str|        Type of the fiber response to be plotted, ``"stress"`` or ``"strain"``. (optional, default is "stress")
   ``skipStart`` |int|        If specified, this many datapoints will be skipped from the data start. (optional, default is 0)
   ``skipEnd`` |int|          If specified, this many datapoints will be skipped from the data end. (optional, default is 0)
   ``rFactor`` |int|          If specified, only every "x" frames will be reduced by this factor. (optional, default is 0)
   ``outputFrames`` |int|     The number of frames to be included after all other reductions. (optional, default is 0)
   ``fps`` |str|              Number of animation frames to be displayed per second. (optional, default is 24)
   ``Xbound`` |list|          ``[xmin, xmax]` The domain of the chart. (optional, default is 1.1 the max and min values)
   ``Ybound`` |float|         ``[ymin, ymax]` The domain of the chart. (optional, default is 1.1 the max and min values)
   ========================  =========================================================================================================


   
Examples: 
    
   ``animate_fiberResponse2D("TwoSpan_Bridge", "Dynamic_GM1", 101, 2)``
                 Animates the fiber stress (default) distribution of section 2 in element 101 of structure by reading data from `TwoSpan_Bridge_ODB` with a sub-folder `Dynamic_GM1` at the last analysis step (default).

