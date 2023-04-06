Modes and Parameters
**********************************

Mode
=======================

In Mist, we provide several modes to meet various demands of users. The following
table demonstrates the performance of three modes against different AI-for-Art
applications.

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

It seems that Fused mode covers the advantage of both Textual and Semantic mode. However, Textural mode is the
most VRAM-saving mode (See in *Device Requirements*) while Semantic mode shows superiority in Textual Inversion.



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