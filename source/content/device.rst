Device Requirements
********************

Different modes of Mist have different VRAM (GPU memory) requirements. 
The following table provides an estimated VRAM cost to run the different 
modes of Mist under different parameters. Please note that all data in the
table is estimated and therefore may differ from the actual situation.


+------------+----------+----------+--------+
|  Low-Vram Mode                            |
+------------+----------+----------+--------+
| resolution | textural | semantic | fused  |
+============+==========+==========+========+
| 256        | 6.4GB    | 10GB     | 10GB   |
+------------+----------+----------+--------+
| 512        | 8GB      | 12GB     | 12GB   |
+------------+----------+----------+--------+
| 768        | 9GB      | 13.4GB   | 13.4GB |
+------------+----------+----------+--------+

  


+------------+----------+----------+-------+
|  Normal Mode                             |
+------------+----------+----------+-------+
| resolution | textural | semantic | fused |
+============+==========+==========+=======+
| 256        | 8GB      | 12GB     | 12GB  |
+------------+----------+----------+-------+
| 512        | 12GB     | 16GB     | 16GB  |
+------------+----------+----------+-------+
| 768        | 24GB     | 32GB     | 32GB  |
+------------+----------+----------+-------+