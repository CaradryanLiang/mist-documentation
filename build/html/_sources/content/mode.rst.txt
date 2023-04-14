Modes and Parameters
**********************************

Mode
=======================

Mist provides three modes for different anti-imitation scenarios. Users can decide which mode to use according to their needs.


Textural mode: By injecting confusing texture information into the watermark to achieve the effect of anti-AI imitation; mainly against Img2Img; requires less GPU memory.


Semantic mode: By interfering with the semantic information of the original image with the watermark; mainly against subject-driven generation (Textual Inversion, Dreambooth, etc.) scenes; requires more GPU memory.


Fused mode: By mixing Textural and Semantic modes in a certain ratio; requires more GPU memory.



The following table demonstrates the performance of the three modes in the four scenarios: Textual Inversion, NovelAI Img2Img, Dreambooth, and Scenario.gg. Among them, Textual Inversion and Dreambooth are both based on Stable Diffusion.

+-------------------------------------------------------+-------------------+-----------------+------------+-------------+
|                                                       | Textual Inversion | NovelAI Img2Img | Dreambooth | Scenario.gg |
+=======================================================+===================+=================+============+=============+
| Textural                                              | ○                 | ◎               | ○          | ◎           |
+-------------------------------------------------------+-------------------+-----------------+------------+-------------+
| Semantic                                              | ◎                 | △               | ╳          | ○           |
+-------------------------------------------------------+-------------------+-----------------+------------+-------------+
| Fused(Fusion weight=1)                                | ◎                 | ○               | △          | ○           |
+-------------------------------------------------------+-------------------+-----------------+------------+-------------+
| ◎:very strong      ○:strong      △:medium      ╳:weak                                                                  |
+-------------------------------------------------------+-------------------+-----------------+------------+-------------+




Parameters
=======================


Mist allows users to customize several parameters that would characterize the watermark. A brief introduction
to these parameters are given in the UI of Mist. The following table further gives some details of these
parameters. 

+---------------+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Parameter     | Recommended value | Note                                                                                                                                                |
+===============+===================+=====================================================================================================================================================+
| Strength      |        16         | 16 promises comprehensive performance in Fused Mode. Relatively, 8 would provide strong performance against certain applications in other two modes.|
+---------------+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Steps         |        100        | 100 is a good tradeoff of time cost and performance.                                                                                                |
+---------------+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Output size   |        512        |                                                                                                                                                     |
+---------------+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Fused weight  |        1          | Fused weight balances the performance tradeoff of Fused mode between Semantic and Textual mode.                                                     |
+---------------+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+
| Low VRAM Mode |       False       | Low VRAM Mode greatly lows down the VRAM requirements with subtly reduced performance.                                                              |
+---------------+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------+